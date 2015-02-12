AC_PREREQ(2.59)
AC_INIT(amz, 0.0.1, jorge.claro@muzzley.com)

AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_AUX_DIR([.])

AM_INIT_AUTOMAKE(foreign)

AC_PROG_INSTALL

LT_INIT

AC_PROG_CXX
AM_PROG_CC_C_O
AC_LANG_CPLUSPLUS

AX_CXX_CHECK_LIB(muzzley,muzzley::HTTPReq,,[AC_MSG_ERROR([No muzzley library could be found])])
dnl Would love to check for something, but free is the easiest
AC_CHECK_LIB(alljoyn,free,,[AC_MSG_ERROR([No alljoyn library could be found])])
AC_CHECK_LIB(alljoyn_about,free,,[AC_MSG_ERROR([No alljoyn_about library could be found])])
AC_CHECK_LIB(alljoyn_config,free,,[AC_MSG_ERROR([No alljoyn_config library could be found])])
AC_CHECK_LIB(alljoyn_controlpanel,free,,[AC_MSG_ERROR([No alljoyn_controlpanel library could be found])])
AC_CHECK_LIB(alljoyn_services_common,free,,[AC_MSG_ERROR([No alljoyn_services_common library could be found])])
dnl I can't get this checks working, so no checks at all for them
dnl AX_CXX_CHECK_LIB(alljoyn_notification,[ajn::services::AsyncTaskQueue::Start ()],,[AC_MSG_ERROR([No alljoyn_notification library could be found])])
dnl AX_CXX_CHECK_LIB(lighting_controller_client,lsf::ControllerClient::AddMethodHandlers,,[AC_MSG_ERROR([No lighting_controller_client library could be found])])

PKG_CHECK_MODULES(OPENSSL_CRYPTO, libcrypto >= 0.0) 
PKG_CHECK_MODULES(GLIB, glib-2.0 >= 1.0)
PKG_CHECK_MODULES(GUPNP, gupnp-1.0 >= 0.1)
PKG_CHECK_MODULES(GSSDP, gssdp-1.0 >= 0.1)
PKG_CHECK_MODULES(XML2, libxml-2.0 >= 2.0)
PKG_CHECK_MODULES(OPENSSL, openssl >= 0.0)
PKG_CHECK_MODULES(OPENSSL_SSL, libssl >= 0.0)



AC_CONFIG_FILES(Makefile
		src/Makefile)

AC_DEFINE(QCC_OS_GROUP_POSIX)
AC_DEFINE(QCC_OS_LINUX)
AC_OUTPUT
