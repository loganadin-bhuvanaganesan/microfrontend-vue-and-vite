<script setup lang="ts">
import Button from "../lib/Button/Button.vue";
import Table from "../lib/Table/Table.vue";
import Input from "../lib/Input/Input.vue";
import { ref } from "vue";
import Timeline from "../lib/Timeline/Timeline.vue";
import JsonView from "../lib/JsonViewer/JsonView.vue";

const inputTest = ref();

const timelineItems = [
  {
    content: "Event start",
    timestamp: "2018-04-15",
  },
  {
    content: "Approved",
    timestamp: "2018-04-13",
  },
  {
    content: "Success",
    timestamp: "2018-04-11",
  },
];

const items = {"shipmentId":"83c11f2a-a8a0-4bcc-bd43-59344057cfef","date":"03-Feb-20","exporter_name":"AKAR TRADING GIDA EMLAK TURIZM ITHALAT VE IHRACAT LIMITED SIRKETI","buyer_name":"AL KAFILE AL ARABIA TRADING. CO","declerant_name":"EGE UZMAN GÜMRÜK MÜSAVIRLIGI VE LOJ","destination_country":"Qatar","origin_country":"Turkey","vehicle_country":"Liberia","hs_code":"20712900000","product_description":"FROZEN UNCHIPPED WHOLE CHICKEN MEAT","unit":"Kilogram","quantity":"46004","total_item_no":"1","item_row_no":"1","statistical_quantity":"46004","gross_weight_kg":"49300","net_weight_kg":"46004","no_of_packages":"2","total_no_of_packages":"3920","invoice_amount":"68499.96","invoice_currency":"USD","unit_price":"1.37","total_value_try":"409122.86","total_value_usd":"62999.96","incoterms":"CIF","mode_of_transport":"Sea","customs_office_name":"Derince Customs","turkey_region":"KOCAELİ","port_of_loading":"Unknown","port_name":"EVYAPPORT KİRAZLIYALI PORT","if_returned_goods":"HAYIR","with_container":"EVET","inspection_line_code":"SARI","system_control_line":"SARI","item_regime_name":"Re-export of goods subjected to inward processing regime conditional exemption system","control_line":"SARI","chapter":"2","heading":"207","sub_heading":"20712","month":"February","year":"2020"};
</script>

<template>
  <Button type="primary">Click here</Button>
  <Table></Table>
  <Input v-model="inputTest" placeholder="Input test"></Input>
  <Timeline :items="timelineItems"></Timeline>
  <JsonView :value="items"></JsonView>

</template>
