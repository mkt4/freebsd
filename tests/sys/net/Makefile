# $FreeBSD$

.include <bsd.own.mk>

TESTSDIR=	${TESTSBASE}/sys/net
BINDIR=		${TESTSDIR}

ATF_TESTS_C+=	if_epair
ATF_TESTS_SH+=	if_bridge_test
ATF_TESTS_SH+=	if_clone_test
ATF_TESTS_SH+=	if_lagg_test
ATF_TESTS_SH+=	if_tun_test
ATF_TESTS_SH+=	if_vlan

TESTS_SUBDIRS+=	routing

# The tests are written to be run in parallel, but doing so leads to random
# panics.  I think it's because the kernel's list of interfaces isn't properly
# locked.
TEST_METADATA+=	is_exclusive=true

MAN=
PROGS+=		randsleep

WARNS?=		6

.include <bsd.test.mk>
