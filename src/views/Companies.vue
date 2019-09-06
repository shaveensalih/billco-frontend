<template>
  <div>
    <base-header type="gradient-success" class="pb-6 pb-8 pt-5 pt-md-8">
      
    </base-header>

    <div class="container-fluid mt--7">
      <div class="row">
        <div class="col">
          <projects-table
            title="Companies"
            :columns="['Company', 'Phone', 'Address', 'Email', ' ']"
            :rows="tableData"
          >
            <template scope="{row}">
              <td>
                <div class="media align-items-center">
                  <a href="#" class="avatar rounded-circle mr-3">
                    <img alt="Image placeholder" :src="row.img" />
                  </a>
                  <div class="media-body">
                    <span class="name mb-0 text-sm">{{row.title}}</span>
                  </div>
                </div>
              </td>
              <td class="budget">{{row.budget}}</td>
              <td>{{row.dateIssued}}</td>
              <td>{{row.dateDue}}</td>
              <td>{{row.daysLeft}}</td>
            </template>
          </projects-table>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ProjectsTable from "./Tables/ProjectsTable";
export default {
  name: "invoices",
  components: {
    ProjectsTable
  }
};
</script>
<style></style>
