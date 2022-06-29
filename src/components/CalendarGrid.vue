<template>
  <div class="px-20 h-full w-full calendar-container">
    <FullCalendar :options="options" class="w-full" />
  </div>
</template>

<script>
import FullCalendar from "@fullcalendar/vue3";
import interactionPlugin from "@fullcalendar/interaction";
import timeGridPlugin from "@fullcalendar/timegrid";
import moment from "moment";

export default {
  name: "CalendarGrid",
  components: {
    FullCalendar,
  },
  data() {
    return {
      options: {
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
        height: 800,
        dayHeaderFormat: { weekday: "short", day: "numeric" },
        slotLabelFormat: {
          hour: "numeric",
          meridiem: "lowercase",
          hour12: true,
        },
        nowIndicator: true,
      },
    };
  },
  methods: {},
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
</style>