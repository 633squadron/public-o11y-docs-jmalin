.. _per-product-limits:

******************************************************
Per product limits in Splunk Observability Cloud
******************************************************

.. meta::
   :description: Separate metric limits alerting for each product.

When you use more than one products in Splunk Observability Cloud to monitor and analyze your data, each product has its own metric time series (MTS) limits. You can set up metric limits alerting to manage your resource usage on a per product basis.

The following table shows per product MTS creation limits.

.. list-table::
   :header-rows: 1
   :widths: 50 50

   * - :strong:`Limit name`
     - :strong:`Default limit value`

   * - :ref:`mts-creations-per-minute-per-product-limit`
     - 6,000 or determined by your subscription
     

.. _mts-creations-per-minute-per-product-limit:

MTS creations per minute per product limit
--------------------------------------------------------------------------------------

   * :strong:`Default limit value`: 6,000 or determined by your subscription.
   * :strong:`Notes`: Maximum number of MTS you can create per minute for each product. For example, if you create 5,500 MTS in the first minute for Infrastructure Monitoring, you can still create 5,500 more in the next minute. You can also create another 6,000 more MTS in the first minute for each other product you use.
   * :strong:`Related metrics`:

     - ``sf.org.numMetricTimeSeriesCreatedByDatapointType``: Number of MTS generated by each product
     - ``sf.org.limit.metricTimeSeriesCreatedPerMinute``: MTS creations per minute limit for Splunk Infrastructure Monitoring in your organization
     - ``sf.org.apm.limit.metricTimeSeriesCreatedPerMinute``: MTS creations per minute limit for Splunk APM in your organization
     - ``sf.org.rum.limit.metricTimeSeriesCreatedPerMinute``: MTS creations per minute limit for Splunk RUM in your organization
     - ``sf.org.synthetics.limit.metricTimeSeriesCreatedPerMinute``: MTS creations per minute limit for Splunk Synthetics in your organization

   * :strong:`Customer impact`: Each product drops new MTS exceeding the limit without returning an error. Data points for existing MTS are still accepted.
