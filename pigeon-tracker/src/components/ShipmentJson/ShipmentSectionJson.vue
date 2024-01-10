<template>
  <div >
    {{ props.shipment }}
    <ShipmentTracking />
    <div>shipmentId</div>
    <div>{{ props.shipment.shipmentId }}</div>
    <div>date</div>
    <div>{{ props.shipment.date }}</div>
    <div>exporter_name</div>
    <div>{{ props.shipment.exporter_name }}</div>
    <div>buyer_name</div>
    <div>{{ props.shipment.buyer_name }}</div>
    <div>declerant_name</div>
    <div>{{ props.shipment.declerant_name }}</div>
    <div>destination_country</div>
    <div>{{ props.shipment.destination_country }}</div>
    <div>origin_country</div>
    <div>{{ props.shipment.origin_country }}</div>
    <div>vehicle_country</div>
    <div>{{ props.shipment.vehicle_country }}</div>
    <div>hs_code</div>
    <div>{{ props.shipment.hs_code }}</div>
  </div>
</template>

<script lang="ts" setup>
import type { Shipment } from "./../Shipment/Shipment";
import ShipmentTracking from "./../Shipment/ShipmentTracking.vue";

const props = defineProps<{
  shipment: Shipment;
}>();
</script>

<style lang="scss" scoped>
.shipmentData {
  display: flex;
  width: 100%;
  gap: 82px;
  margin-top: 30px;
  max-width: 1000px;
}
</style>
