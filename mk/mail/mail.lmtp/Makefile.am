include	$(top_srcdir)/mk/pathnames

pkglibexec_PROGRAMS =	mail.lmtp

mail_lmtp_SOURCES = $(top_srcdir)/usr.sbin/smtpd/mail.lmtp.c
mail_lmtp_SOURCES+= $(top_srcdir)/usr.sbin/smtpd/log.c

dist_man8_MANS =	$(top_srcdir)/usr.sbin/smtpd/mail.lmtp.8

AM_CPPFLAGS=		-I$(top_srcdir)/usr.sbin/smtpd \
			-I$(top_srcdir)/openbsd-compat

LDADD = 		$(LIBOBJS)

uninstall-hook:
	rmdir	$(DESTDIR)$(pkglibexecdir) 2> /dev/null || true
