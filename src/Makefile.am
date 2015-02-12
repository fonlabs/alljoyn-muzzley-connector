bin_PROGRAMS = amz
amz_SOURCES = alljoyn_muzzley_connector.cc \
	      AnnounceHandlerImpl.cc \
	      ControlPanelListenerImpl.cc \
	      ControllerNotificationReceiver.cc 

amz_CPPFLAGS = -I../include \
		$(XML2_CFLAGS) \
		$(GUPNP_CFLAGS) \
		$(OPENSSL_SSL_CFLAGS) \
		$(OPENSSL_CRYPTO_CFLAGS) \
		$(OPENSSL_CFLAGS) \
		-std=gnu++0x

amz_LDADD = -lpthread \
	    $(XML2_LIBS) \
	    $(GLIB_LIBS) \
	    $(GUPNP_LIBS) \
	    $(GSSDP_LIBS) \
	    $(OPENSSL_SSL_LIBS) \
	    $(OPENSSL_CRYPTO_LIBS) \
	    $(OPENSSL_LIBS) \
	    -lalljoyn \
	    -lalljoyn_about \
	    -lalljoyn_config \
	    -lalljoyn_controlpanel \
	    -lalljoyn_notification \
	    -lalljoyn_services_common \
	    -llighting_controller_client
