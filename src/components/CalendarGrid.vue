<template>
  <div
    class="
      hidden
      md:block
      px-20
      h-full
      w-full
      calendar-container
      -z-10
      relative
    "
  >
    <FullCalendar :options="options" class="w-full" />
  </div>
</template>

<script>
import FullCalendar from "@fullcalendar/vue3";
import interactionPlugin from "@fullcalendar/interaction";
import timeGridPlugin from "@fullcalendar/timegrid";
import EventData from "./EventData";

export default {
  name: "CalendarGrid",
  components: {
    FullCalendar,
  },
  data() {
    return {
      options: {
        events: EventData,
        themeSystem: "standard",
        plugins: [timeGridPlugin, interactionPlugin],
        scrollTime: "09:00:00",
        headerToolbar: {
          start: "",
          center: "",
          end: "",
        },
        slotDuration: "01:00:00",
        initialView: "timeGridWeek",
        allDaySlot: false,
        firstDay: 0,
        expandRows: true,
        height: "72vh",
        dayHeaderFormat: { weekday: "short", day: "numeric" },
        slotLabelFormat: {
          hour: "numeric",
          meridiem: "lowercase",
          hour12: true,
        },
        nowIndicator: true,
        eventBackgroundColor: "#fff",
        eventTextColor: "#000",
        eventTimeFormat: {
          hour: "numeric",
          minute: "2-digit",
          meridiem: "lowercase",
          omitZeroMinute: true,
        },
        displayEventEnd: false,
      },
    };
  },
};
</script>

<style >
table {
  border: 0px !important;
  font-size: 15px !important;
}
tbody tr,
tbody td {
  height: 80px;
}
thead,
th {
  border-top: 0px !important;
  height: 30px !important;
}

table tr:last-child td {
  border-bottom: 0px !important;
}
table,
th,
table tr td:first-child {
  border-left: 0px !important;
}
thead th:last-child,
table tr td:last-child {
  border-right: 0px !important;
}

.fc-timegrid-slot {
  padding-right: 10px !important;
}

.fc-day-today {
  background-color: transparent !important;
}

.fc-timegrid-now-indicator-line {
  border-color: #00dcdc !important;
  border-width: 1px !important;
  height: 1px;
}

.fc-timegrid-now-indicator-line::before {
  content: "";
  border-color: #00dcdc !important;
  border-radius: 9999px !important;
  border-width: 5px !important;
  height: 5px;
  position: absolute;
  top: -5px;
  left: -1px;
}
.fc-timegrid-now-indicator-arrow {
  display: none !important;
}

.fc-day-past {
  background-color: #fafafa !important;
}

.fc-col-header-cell {
  background-color: transparent !important;
}

.fc-timegrid-event {
  border-radius: 4px 0 4px 0 !important;
  font-size: 12px !important;
  border-width: 0.1rem !important;
  width: 80%;
}
.fc-event-time {
  font-weight: 600 !important;
  font-size: 12px !important;
  margin-top: 3px;
}
.fc-v-event .fc-event-main-frame {
  flex-direction: column-reverse !important;
  justify-content: start;
  padding-left: 15px !important;
  position: relative;
  top: -100%;
}
.fc-v-event .fc-event-title-container {
  flex-grow: 0 !important;
  flex-shrink: 0 !important;
}
.fc-event-main::before {
  content: "";
  height: 102%;
  background-color: #394ced;
  border-color: #394ced;
  border-radius: 4px 0 4px 0;
  width: 10px !important;
  display: inline-block;
  position: relative;
  top: -1px;
  left: -2px;
}
.createdMeeow .fc-event-main::before {
  background-color: #00dcdc;
  border-color: #00dcdc;
}
.bookedMeeow .fc-event-main::before {
  background-color: #9231ce;
  border-color: #9231ce;
}
.onDemandMeeow .fc-event-main::before {
  background-color: #394ced;
  border-color: #394ced;
}
.suggestedMeeow .fc-event-main::before {
  background-color: #000;
  border-color: #000;
}
</style>