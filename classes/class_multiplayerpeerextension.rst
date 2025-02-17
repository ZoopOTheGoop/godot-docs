:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/MultiplayerPeerExtension.xml.

.. _class_MultiplayerPeerExtension:

MultiplayerPeerExtension
========================

**Inherits:** :ref:`MultiplayerPeer<class_MultiplayerPeer>` **<** :ref:`PacketPeer<class_PacketPeer>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

Class that can be inherited to implement custom multiplayer API networking layers via GDExtension.

Description
-----------

This class is designed to be inherited from a GDExtension plugin to implement custom networking layers for the multiplayer API (such as WebRTC). All the methods below **must** be implemented to have a working custom multiplayer implementation. See also :ref:`MultiplayerAPI<class_MultiplayerAPI>`.

Methods
-------

+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_close<class_MultiplayerPeerExtension_method__close>` **(** **)** |virtual|                                                                                       |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_disconnect_peer<class_MultiplayerPeerExtension_method__disconnect_peer>` **(** :ref:`int<class_int>` p_peer, :ref:`bool<class_bool>` p_force **)** |virtual|     |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                                          | :ref:`_get_available_packet_count<class_MultiplayerPeerExtension_method__get_available_packet_count>` **(** **)** |virtual| |const|                                     |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`ConnectionStatus<enum_MultiplayerPeer_ConnectionStatus>` | :ref:`_get_connection_status<class_MultiplayerPeerExtension_method__get_connection_status>` **(** **)** |virtual| |const|                                               |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                                          | :ref:`_get_max_packet_size<class_MultiplayerPeerExtension_method__get_max_packet_size>` **(** **)** |virtual| |const|                                                   |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@GlobalScope_Error>`                          | :ref:`_get_packet<class_MultiplayerPeerExtension_method__get_packet>` **(** const uint8_t ** r_buffer, int32_t* r_buffer_size **)** |virtual|                           |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                                          | :ref:`_get_packet_peer<class_MultiplayerPeerExtension_method__get_packet_peer>` **(** **)** |virtual| |const|                                                           |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PackedByteArray<class_PackedByteArray>`                  | :ref:`_get_packet_script<class_MultiplayerPeerExtension_method__get_packet_script>` **(** **)** |virtual|                                                               |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                                          | :ref:`_get_transfer_channel<class_MultiplayerPeerExtension_method__get_transfer_channel>` **(** **)** |virtual| |const|                                                 |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`TransferMode<enum_MultiplayerPeer_TransferMode>`         | :ref:`_get_transfer_mode<class_MultiplayerPeerExtension_method__get_transfer_mode>` **(** **)** |virtual| |const|                                                       |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                                          | :ref:`_get_unique_id<class_MultiplayerPeerExtension_method__get_unique_id>` **(** **)** |virtual| |const|                                                               |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                                        | :ref:`_is_refusing_new_connections<class_MultiplayerPeerExtension_method__is_refusing_new_connections>` **(** **)** |virtual| |const|                                   |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                                        | :ref:`_is_server<class_MultiplayerPeerExtension_method__is_server>` **(** **)** |virtual| |const|                                                                       |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_poll<class_MultiplayerPeerExtension_method__poll>` **(** **)** |virtual|                                                                                         |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@GlobalScope_Error>`                          | :ref:`_put_packet<class_MultiplayerPeerExtension_method__put_packet>` **(** const uint8_t* p_buffer, :ref:`int<class_int>` p_buffer_size **)** |virtual|                |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@GlobalScope_Error>`                          | :ref:`_put_packet_script<class_MultiplayerPeerExtension_method__put_packet_script>` **(** :ref:`PackedByteArray<class_PackedByteArray>` p_buffer **)** |virtual|        |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_set_refuse_new_connections<class_MultiplayerPeerExtension_method__set_refuse_new_connections>` **(** :ref:`bool<class_bool>` p_enable **)** |virtual|            |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_set_target_peer<class_MultiplayerPeerExtension_method__set_target_peer>` **(** :ref:`int<class_int>` p_peer **)** |virtual|                                      |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_set_transfer_channel<class_MultiplayerPeerExtension_method__set_transfer_channel>` **(** :ref:`int<class_int>` p_channel **)** |virtual|                         |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                           | :ref:`_set_transfer_mode<class_MultiplayerPeerExtension_method__set_transfer_mode>` **(** :ref:`TransferMode<enum_MultiplayerPeer_TransferMode>` p_mode **)** |virtual| |
+----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Method Descriptions
-------------------

.. _class_MultiplayerPeerExtension_method__close:

- void **_close** **(** **)** |virtual|

Called when the multiplayer peer should be immediately closed (see :ref:`MultiplayerPeer.close<class_MultiplayerPeer_method_close>`).

----

.. _class_MultiplayerPeerExtension_method__disconnect_peer:

- void **_disconnect_peer** **(** :ref:`int<class_int>` p_peer, :ref:`bool<class_bool>` p_force **)** |virtual|

Called when the connected ``p_peer`` should be forcibly disconnected (see :ref:`MultiplayerPeer.disconnect_peer<class_MultiplayerPeer_method_disconnect_peer>`).

----

.. _class_MultiplayerPeerExtension_method__get_available_packet_count:

- :ref:`int<class_int>` **_get_available_packet_count** **(** **)** |virtual| |const|

Called when the available packet count is internally requested by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`.

----

.. _class_MultiplayerPeerExtension_method__get_connection_status:

- :ref:`ConnectionStatus<enum_MultiplayerPeer_ConnectionStatus>` **_get_connection_status** **(** **)** |virtual| |const|

Called when the connection status is requested on the :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.get_connection_status<class_MultiplayerPeer_method_get_connection_status>`).

----

.. _class_MultiplayerPeerExtension_method__get_max_packet_size:

- :ref:`int<class_int>` **_get_max_packet_size** **(** **)** |virtual| |const|

Called when the maximum allowed packet size (in bytes) is requested by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`.

----

.. _class_MultiplayerPeerExtension_method__get_packet:

- :ref:`Error<enum_@GlobalScope_Error>` **_get_packet** **(** const uint8_t ** r_buffer, int32_t* r_buffer_size **)** |virtual|

Called when a packet needs to be received by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`, with ``r_buffer_size`` being the size of the binary ``r_buffer`` in bytes.

----

.. _class_MultiplayerPeerExtension_method__get_packet_peer:

- :ref:`int<class_int>` **_get_packet_peer** **(** **)** |virtual| |const|

Called when the ID of the :ref:`MultiplayerPeer<class_MultiplayerPeer>` who sent the most recent packet is requested (see :ref:`MultiplayerPeer.get_packet_peer<class_MultiplayerPeer_method_get_packet_peer>`).

----

.. _class_MultiplayerPeerExtension_method__get_packet_script:

- :ref:`PackedByteArray<class_PackedByteArray>` **_get_packet_script** **(** **)** |virtual|

Called when a packet needs to be received by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`, if :ref:`_get_packet<class_MultiplayerPeerExtension_method__get_packet>` isn't implemented. Use this when extending this class via GDScript.

----

.. _class_MultiplayerPeerExtension_method__get_transfer_channel:

- :ref:`int<class_int>` **_get_transfer_channel** **(** **)** |virtual| |const|

Called when the transfer channel to use is read on this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.transfer_channel<class_MultiplayerPeer_property_transfer_channel>`).

----

.. _class_MultiplayerPeerExtension_method__get_transfer_mode:

- :ref:`TransferMode<enum_MultiplayerPeer_TransferMode>` **_get_transfer_mode** **(** **)** |virtual| |const|

Called when the transfer mode to use is read on this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.transfer_mode<class_MultiplayerPeer_property_transfer_mode>`).

----

.. _class_MultiplayerPeerExtension_method__get_unique_id:

- :ref:`int<class_int>` **_get_unique_id** **(** **)** |virtual| |const|

Called when the unique ID of this :ref:`MultiplayerPeer<class_MultiplayerPeer>` is requested (see :ref:`MultiplayerPeer.get_unique_id<class_MultiplayerPeer_method_get_unique_id>`).

----

.. _class_MultiplayerPeerExtension_method__is_refusing_new_connections:

- :ref:`bool<class_bool>` **_is_refusing_new_connections** **(** **)** |virtual| |const|

Called when the "refuse new connections" status is requested on this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.refuse_new_connections<class_MultiplayerPeer_property_refuse_new_connections>`).

----

.. _class_MultiplayerPeerExtension_method__is_server:

- :ref:`bool<class_bool>` **_is_server** **(** **)** |virtual| |const|

Called when the "is server" status is requested on the :ref:`MultiplayerAPI<class_MultiplayerAPI>`. See :ref:`MultiplayerAPI.is_server<class_MultiplayerAPI_method_is_server>`.

----

.. _class_MultiplayerPeerExtension_method__poll:

- void **_poll** **(** **)** |virtual|

Called when the :ref:`MultiplayerAPI<class_MultiplayerAPI>` is polled. See :ref:`MultiplayerAPI.poll<class_MultiplayerAPI_method_poll>`.

----

.. _class_MultiplayerPeerExtension_method__put_packet:

- :ref:`Error<enum_@GlobalScope_Error>` **_put_packet** **(** const uint8_t* p_buffer, :ref:`int<class_int>` p_buffer_size **)** |virtual|

Called when a packet needs to be sent by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`, with ``p_buffer_size`` being the size of the binary ``p_buffer`` in bytes.

----

.. _class_MultiplayerPeerExtension_method__put_packet_script:

- :ref:`Error<enum_@GlobalScope_Error>` **_put_packet_script** **(** :ref:`PackedByteArray<class_PackedByteArray>` p_buffer **)** |virtual|

Called when a packet needs to be sent by the :ref:`MultiplayerAPI<class_MultiplayerAPI>`, if :ref:`_put_packet<class_MultiplayerPeerExtension_method__put_packet>` isn't implemented. Use this when extending this class via GDScript.

----

.. _class_MultiplayerPeerExtension_method__set_refuse_new_connections:

- void **_set_refuse_new_connections** **(** :ref:`bool<class_bool>` p_enable **)** |virtual|

Called when the "refuse new connections" status is set on this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.refuse_new_connections<class_MultiplayerPeer_property_refuse_new_connections>`).

----

.. _class_MultiplayerPeerExtension_method__set_target_peer:

- void **_set_target_peer** **(** :ref:`int<class_int>` p_peer **)** |virtual|

Called when the target peer to use is set for this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.set_target_peer<class_MultiplayerPeer_method_set_target_peer>`).

----

.. _class_MultiplayerPeerExtension_method__set_transfer_channel:

- void **_set_transfer_channel** **(** :ref:`int<class_int>` p_channel **)** |virtual|

Called when the channel to use is set for this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.transfer_channel<class_MultiplayerPeer_property_transfer_channel>`).

----

.. _class_MultiplayerPeerExtension_method__set_transfer_mode:

- void **_set_transfer_mode** **(** :ref:`TransferMode<enum_MultiplayerPeer_TransferMode>` p_mode **)** |virtual|

Called when the transfer mode is set on this :ref:`MultiplayerPeer<class_MultiplayerPeer>` (see :ref:`MultiplayerPeer.transfer_mode<class_MultiplayerPeer_property_transfer_mode>`).

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
