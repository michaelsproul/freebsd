# $FreeBSD$

.include <src.opts.mk>

FILES=	DAEMON \
	FILESYSTEMS \
	LOGIN \
	NETWORKING \
	SERVERS \
	abi \
	accounting \
	addswap \
	adjkerntz \
	archdep \
	atm1 \
	atm2 \
	atm3 \
	auditd \
	auditdistd \
	bgfsck \
	${_bluetooth} \
	bootparams \
	bridge \
	${_bthidd} \
	${_casperd} \
	cleanvar \
	cleartmp \
	cron \
	ctld \
	ddb \
	defaultroute \
	devd \
	devfs \
	dhclient \
	dmesg \
	dumpon \
	fsck \
	ftpd \
	gbde \
	geli \
	geli2 \
	gptboot \
	growfs \
	gssd \
	${_hcsecd} \
	hostapd \
	hostid \
	hostid_save \
	hostname \
	inetd \
	ip6addrctl \
	ipfilter \
	ipfs \
	ipfw \
	ipmon \
	ipnat \
	ipsec \
	${_kadmind} \
	${_kdc} \
	${_kfd} \
	kld \
	kldxref \
	${_kpasswdd} \
	ldconfig \
	local \
	localpkg \
	lockd \
	mixer \
	motd \
	mountcritlocal \
	mountcritremote \
	mountlate \
	mdconfig \
	mdconfig2 \
	mountd \
	moused \
	mroute6d \
	msgs \
	natd \
	netif \
	netoptions \
	netwait \
	newsyslog \
	nfsclient \
	nfscbd \
	nfsd \
	nfsuserd \
	nisdomain \
	${_nscd} \
	nsswitch \
	ntpd \
	ntpdate \
	${_opensm} \
	othermta \
	pf \
	pflog \
	pfsync \
	powerd \
	ppp \
	pppoed \
	pwcheck \
	quota \
	random \
	rarpd \
	rctl \
	resolv \
	rfcomm_pppd_server \
	root \
	route6d \
	routed \
	routing \
	rpcbind \
	rtadvd \
	rtsold \
	savecore \
	sdpd \
	securelevel \
	sendmail \
	serial \
	sppp \
	${_sshd} \
	statd \
	static_arp \
	static_ndp \
	stf \
	swap \
	swaplate \
	syscons \
	sysctl \
	syslogd \
	timed \
	tmp \
	${_ubthidhci} \
	ugidfw \
	${_unbound} \
	${_utx} \
	var \
	virecover \
	watchdogd \
	wpa_supplicant \
	ypbind \
	yppasswdd \
	ypserv \
	ypset \
	ypupdated \
	ypxfrd \
	zfs \
	zvol

.if ${MK_ACCT} != "no"
FILES+=		accounting
.endif

.if ${MK_ACPI} != "no"
FILES+=		power_profile
.endif

.if ${MK_AMD} != "no"
FILES+=		amd
.endif

.if ${MK_APM} != "no"
FILES+=	apm
FILES+=	apmd
.endif

.if ${MK_AUTOFS} != "no"
FILES+=		automount
FILES+=		automountd
FILES+=		autounmountd
.endif

.if ${MK_BLUETOOTH} != "no"
_bluetooth=	bluetooth
_bthidd=	bthidd
_hcsecd=	hcsecd
_ubthidhci=	ubthidhci
.endif

.if ${MK_BSNMP} != "no"
FILES+=		bsnmpd
.endif

.if ${MK_CASPER} != "no"
_casperd=	casperd
.endif

.if ${MK_CCD} != "no"
FILES+=		ccd
.endif

.if ${MK_HAST} != "no"
FILES+=		hastd
.endif

.if ${MK_ISCSI} != "no"
FILES+=		iscsictl
FILES+=		iscsid
.endif

.if ${MK_JAIL} != "no"
FILES+=	jail
.endif

.if ${MK_LPR} != "no"
FILES+=		lpd
.endif

.if ${MK_NS_CACHING} != "no"
_nscd=		nscd
.endif

.if ${MK_KERBEROS} != "no"
FILES+=		ipropd_master
FILES+=		ipropd_slave
_kadmind=	kadmind
_kdc=		kdc
_kfd=		kfd
_kpasswdd=	kpasswdd
.endif

.if ${MK_OFED} != "no"
_opensm=	opensm
.endif

.if ${MK_OPENSSL} != "no"
FILES+=		keyserv
.endif

.if ${MK_OPENSSH} != "no"
_sshd=		sshd
.endif

.if ${MK_PF} != "no"
FILES+=		ftp-proxy
.endif

.if ${MK_RCMDS} != "no"
FILES+=		rwho
.endif

.if ${MK_UNBOUND} != "no"
_unbound=	local_unbound
.endif

.if ${MK_UTMPX} != "no"
_utx=		utx
.endif

.if ${MK_WIRELESS} != "no"
FILES+=		hostapd
FILES+=		wpa_supplicant
.endif

FILESDIR=	/etc/rc.d
FILESMODE=	${BINMODE}

.include <bsd.prog.mk>
