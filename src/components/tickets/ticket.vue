<template>
  <tr>
    <td class="pl-0">
      <div class="icon-rounded-primary icon-rounded-md">
        <h4 class="font-weight-medium">{{this.getInitials(ticket.name)}}</h4>
      </div>
    </td>
    <td>
      <p class="mb-0">{{ticket.name}}</p>
      <p class="text-muted mb-0">{{ticket.city}}</p>
    </td>
    <td>
      <p class="mb-0">{{getDateParts(ticket.date)[0]}}</p>
      <p class="text-muted mb-0">{{getDateParts(ticket.date)[1]}}</p>
    </td>
    <td>
      <p class="mb-0">{{ticket.project}}</p>
      <p class="text-muted mb-0">{{ticket.other}}</p>
    </td>
    <td class="pr-0">
      <i class="mdi mdi-dots-horizontal icon-sm cursor-pointer"></i>
    </td>
  </tr>
</template>

<script>
export default {
  name: "Ticket",
  props: {
    ticket: Object
  },
  methods: {
     getInitials: (name) => {
            let names = name.split(" ");
            let initials = names[0][0] + names[1][0]; 

            return initials;
        },
    getDateParts: (date) => {
        let dateParts = date.split(", ");
        return dateParts;
    }
  }
};
</script>

<style>
</style>