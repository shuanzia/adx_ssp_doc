对接关键点
==========

.. warning:: 此处列出的所有对接项请自行阅读，并检查是否都已经符合要求，否则广告在投放过程中，将会出现流量被屏蔽，填充不高，收益较低等问题，请仔细核查检验


客户端UA和IP地址上报
--------------------

请确认 ``客户端UA`` 和 ``客户端IP地址`` 通过 ``http header头`` 在请求ADX的时候，传到ADX

.. warning:: 客户端UA,IP 如果不通过header传过来，将会取服务端的IP做为客户端地址, adx会将重复过多的IP当做作弊流量被屏蔽掉

曝光和点击多地址上报问题
------------------------

 * 所有的地址均应由客户端发起请求，禁止服务端请求
 * ADX返回的 ``imp_trackers`` ``click_trackers`` 为一个数组，请确保所有的地址均可以被触发
 * 如果是由 ``html`` 中的 ``js`` 来触发,请确保在点击跳转的时候，请确保数组中的每个地址都被触发，不要因页面跳转导致丢失

.. warning:: 如果多地址中的请求有未被触发的，会影响最终的结算


传递参数校验
------------

* android请求中 请务必将  ``imei`` 传递

* ios请求中，请务必将设备的  ``idfa`` 传递

