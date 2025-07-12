<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.42-33`](#percona8042-33)
-	[`percona:8.0.42-33-centos`](#percona8042-33-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.42-33`](#perconaps-8042-33)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.24`](#perconapsmdb-6024)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.18`](#perconapsmdb-7018)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.8`](#perconapsmdb-808)

## `percona:8`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.42-33`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.42-33` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.42-33` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.42-33-centos`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.42-33-centos` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.42-33-centos` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.42-33`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.42-33` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.42-33` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:471a867eede290d2ef926516dda4cd6f3a45fd1a4134b9219eb3bdf56b812675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:afc4cb0a72829e1dc4660f60e9faa8ce645c3092a804d6e603c6467a88165603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254128962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee715c58baf8a12a38abed0dd9934e01351587c3373c77fdd4655a2c8716896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=6.0.24-19
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=6.0.24-19.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=release
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64953ab748f36a795befd74abf4063061fe05df8cd7f9999930525c106f015a7`  
		Last Modified: Fri, 11 Jul 2025 23:34:01 GMT  
		Size: 8.5 MB (8485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556b6b542ac0853538d9259203188491885ea5bfb913063c03a2beea0b7c791b`  
		Last Modified: Sat, 12 Jul 2025 02:13:17 GMT  
		Size: 205.0 MB (205033683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1908508d72ec5abce27df3c5367878b1e2847ab6deb35d03b13197979db6202b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722eed0ff7f5cf00d586e41fd739ba239a5e982fae6e27061ff43040ff41ed02`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b986a3da8d36529e64e4df5fa562c1d00a289adf449f519a937b9890273cf72`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ea2a25f53065ba9c10482fb46e664fe58b5857ade5dc331cf1f710400c3e06`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c5b5b057ba9244e8a57df6a21c6ce68c318559a76086e92869288d9896fb8`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6982a8cfde517acb45fe3d8dcd6e647f591b6e1349ea5b697e82c9494329a7a3`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349550007b733877149b50f499ce674e67d247036874e319f5fee57c796a678b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:9d15da33982c7144889b97a7156c1eec82c3418a005a00db72797e4e87df4f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d47d559c1172e2e879f1cc77cfc686b3cbd62f85336057355f099ab8ed7835b`

```dockerfile
```

-	Layers:
	-	`sha256:a0f159fbed0c3707fc619f4e715539e8e37c0c8a91f4b8fb88b0d1af50bdcb63`  
		Last Modified: Sat, 12 Jul 2025 02:10:30 GMT  
		Size: 32.7 KB (32657 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.24`

```console
$ docker pull percona@sha256:471a867eede290d2ef926516dda4cd6f3a45fd1a4134b9219eb3bdf56b812675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.24` - linux; amd64

```console
$ docker pull percona@sha256:afc4cb0a72829e1dc4660f60e9faa8ce645c3092a804d6e603c6467a88165603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254128962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee715c58baf8a12a38abed0dd9934e01351587c3373c77fdd4655a2c8716896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=6.0.24-19
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=6.0.24-19.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=release
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64953ab748f36a795befd74abf4063061fe05df8cd7f9999930525c106f015a7`  
		Last Modified: Fri, 11 Jul 2025 23:34:01 GMT  
		Size: 8.5 MB (8485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556b6b542ac0853538d9259203188491885ea5bfb913063c03a2beea0b7c791b`  
		Last Modified: Sat, 12 Jul 2025 02:13:17 GMT  
		Size: 205.0 MB (205033683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1908508d72ec5abce27df3c5367878b1e2847ab6deb35d03b13197979db6202b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722eed0ff7f5cf00d586e41fd739ba239a5e982fae6e27061ff43040ff41ed02`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b986a3da8d36529e64e4df5fa562c1d00a289adf449f519a937b9890273cf72`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ea2a25f53065ba9c10482fb46e664fe58b5857ade5dc331cf1f710400c3e06`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c5b5b057ba9244e8a57df6a21c6ce68c318559a76086e92869288d9896fb8`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6982a8cfde517acb45fe3d8dcd6e647f591b6e1349ea5b697e82c9494329a7a3`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349550007b733877149b50f499ce674e67d247036874e319f5fee57c796a678b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.24` - unknown; unknown

```console
$ docker pull percona@sha256:9d15da33982c7144889b97a7156c1eec82c3418a005a00db72797e4e87df4f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d47d559c1172e2e879f1cc77cfc686b3cbd62f85336057355f099ab8ed7835b`

```dockerfile
```

-	Layers:
	-	`sha256:a0f159fbed0c3707fc619f4e715539e8e37c0c8a91f4b8fb88b0d1af50bdcb63`  
		Last Modified: Sat, 12 Jul 2025 02:10:30 GMT  
		Size: 32.7 KB (32657 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:2d6118f4d11c9a85dda1c1e047771a7098567623e97abceb6d3de73b5ab8f8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:16fc69b089978f60e9f9f8145521fed804232780ef2f27953025823af8c2713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269218795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0058f15d7daa8f591015736a7780a16df1b14d2031d06ead85ffdb5db6c85108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=7.0.18-11
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=7.0.18-11.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=release
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0da90dfebcb299ff9cb89d2d0d8cd2e783ca36f9b8a1cb066b58d20cf0801c`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 8.5 MB (8481289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27177bb509eb98f62fcaeafb5beb20b3f624767723ae6d7101cf98460984b187`  
		Last Modified: Sat, 12 Jul 2025 02:15:24 GMT  
		Size: 220.1 MB (220127878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577c4a7d4d99b2c2871b10d0fc4b7d392760e1b70fcbcc94594351c0c23fefe`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57ed847744e4667f2093fb8f0918c22c70467690f9640ab7877182e5b2ff116`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000745fad3d0691e85ec397a5b3cf648806db686489f123b2998047cc3e713ec`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b0844664c4aef9027e8e8ef8002d2840cca068e6aa113385b582f668dd0450`  
		Last Modified: Fri, 11 Jul 2025 23:33:56 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b15d666a91ba2d271f4247cf97c7db8c7340b9639e0561b3efd7137372665`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfa7a968cce8cf3e95c82293dd0594b9d928317a0e5c59556234d877a78cb0`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cab42d3c28e985500340a0643faae66ce72ff9dbcb15cd41d211ae7fb0a5a9`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:5b431c121af908ea25038fac225206889d8f48a6e00b25cbd526df859b021dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c213b3ffd1a2b8744869d0036754c3f259945f7ef0490b1fe7aedcf2f2296`

```dockerfile
```

-	Layers:
	-	`sha256:b6775a52539eb9d6de092ebd7ed7caa559bdce5bf719c2c4bad8b7048f33e4e6`  
		Last Modified: Sat, 12 Jul 2025 02:10:36 GMT  
		Size: 32.2 KB (32166 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.18`

```console
$ docker pull percona@sha256:2d6118f4d11c9a85dda1c1e047771a7098567623e97abceb6d3de73b5ab8f8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.18` - linux; amd64

```console
$ docker pull percona@sha256:16fc69b089978f60e9f9f8145521fed804232780ef2f27953025823af8c2713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269218795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0058f15d7daa8f591015736a7780a16df1b14d2031d06ead85ffdb5db6c85108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=7.0.18-11
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=7.0.18-11.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=release
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0da90dfebcb299ff9cb89d2d0d8cd2e783ca36f9b8a1cb066b58d20cf0801c`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 8.5 MB (8481289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27177bb509eb98f62fcaeafb5beb20b3f624767723ae6d7101cf98460984b187`  
		Last Modified: Sat, 12 Jul 2025 02:15:24 GMT  
		Size: 220.1 MB (220127878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577c4a7d4d99b2c2871b10d0fc4b7d392760e1b70fcbcc94594351c0c23fefe`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57ed847744e4667f2093fb8f0918c22c70467690f9640ab7877182e5b2ff116`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000745fad3d0691e85ec397a5b3cf648806db686489f123b2998047cc3e713ec`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b0844664c4aef9027e8e8ef8002d2840cca068e6aa113385b582f668dd0450`  
		Last Modified: Fri, 11 Jul 2025 23:33:56 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b15d666a91ba2d271f4247cf97c7db8c7340b9639e0561b3efd7137372665`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfa7a968cce8cf3e95c82293dd0594b9d928317a0e5c59556234d877a78cb0`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cab42d3c28e985500340a0643faae66ce72ff9dbcb15cd41d211ae7fb0a5a9`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.18` - unknown; unknown

```console
$ docker pull percona@sha256:5b431c121af908ea25038fac225206889d8f48a6e00b25cbd526df859b021dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c213b3ffd1a2b8744869d0036754c3f259945f7ef0490b1fe7aedcf2f2296`

```dockerfile
```

-	Layers:
	-	`sha256:b6775a52539eb9d6de092ebd7ed7caa559bdce5bf719c2c4bad8b7048f33e4e6`  
		Last Modified: Sat, 12 Jul 2025 02:10:36 GMT  
		Size: 32.2 KB (32166 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:d96060579df6ab8e9a75c2e13a25c6c0ca928296bfb5ff7fd11508c425282ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:cd590e2f4d2f080703f7df383c218219971472cc6bffdd2cabb5da864fc6080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286289908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c5262e6dc5785e235f0ae768a685f2609b72e04cfc397255a5f3cdb8470ba6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=8.0.8-3
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=8.0.8-3.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=testing
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca3d9ef565b138009d628d3c6253e1d3425197689bfe9968a4152fd53097b56`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 8.5 MB (8481287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba10af1c55f51269cf5b59ba78d7c1d22237b16a7621f974b9f4873ef47cb7f`  
		Last Modified: Sat, 12 Jul 2025 02:12:19 GMT  
		Size: 237.2 MB (237199006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec50023ccd8ff9ca400577eaef3d2c17569e91e97e4a47ed4a5a1164d6fa02b5`  
		Last Modified: Fri, 11 Jul 2025 23:33:53 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24df55408ed06ec73b459678e2b271ef170bd32db6b0c0c5de3b1a0db89f44`  
		Last Modified: Fri, 11 Jul 2025 23:33:53 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd73283749bffb9fa609d03b011d2eab0664d984b0fe3f7b7328e2762ab70f`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64aecedb9ec847d868186f50a221219c534ef558327db7eb0e25792a9567fdc`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef67510816ce4adaff51f30554e60c883869f67f78dfcb679c5f9c58d7a8d5e`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20eb31da817d8d6e214d5e1d1125137e31642fec2501061f3cf906337049433`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc530b8590c78ee1cb17f16ab3d0bc2488de6fac66a1faa09d9d0c12cab51ed`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:3fff02cacad185d53949367226152f1a8d51e1e6fd8791a277cba51e77b9cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ef0c46496d90e0e3ceb18a1672191ac176a4ad8c5333b2aa3dddd189edfae5`

```dockerfile
```

-	Layers:
	-	`sha256:d5147d83cbd03ee45eef34427467bbfb0f7c7e78d9bc3d75348a783b4dd8598c`  
		Last Modified: Sat, 12 Jul 2025 02:10:40 GMT  
		Size: 32.4 KB (32437 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.8`

```console
$ docker pull percona@sha256:d96060579df6ab8e9a75c2e13a25c6c0ca928296bfb5ff7fd11508c425282ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.8` - linux; amd64

```console
$ docker pull percona@sha256:cd590e2f4d2f080703f7df383c218219971472cc6bffdd2cabb5da864fc6080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286289908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c5262e6dc5785e235f0ae768a685f2609b72e04cfc397255a5f3cdb8470ba6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=8.0.8-3
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=8.0.8-3.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=testing
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca3d9ef565b138009d628d3c6253e1d3425197689bfe9968a4152fd53097b56`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 8.5 MB (8481287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba10af1c55f51269cf5b59ba78d7c1d22237b16a7621f974b9f4873ef47cb7f`  
		Last Modified: Sat, 12 Jul 2025 02:12:19 GMT  
		Size: 237.2 MB (237199006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec50023ccd8ff9ca400577eaef3d2c17569e91e97e4a47ed4a5a1164d6fa02b5`  
		Last Modified: Fri, 11 Jul 2025 23:33:53 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24df55408ed06ec73b459678e2b271ef170bd32db6b0c0c5de3b1a0db89f44`  
		Last Modified: Fri, 11 Jul 2025 23:33:53 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd73283749bffb9fa609d03b011d2eab0664d984b0fe3f7b7328e2762ab70f`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64aecedb9ec847d868186f50a221219c534ef558327db7eb0e25792a9567fdc`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef67510816ce4adaff51f30554e60c883869f67f78dfcb679c5f9c58d7a8d5e`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20eb31da817d8d6e214d5e1d1125137e31642fec2501061f3cf906337049433`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc530b8590c78ee1cb17f16ab3d0bc2488de6fac66a1faa09d9d0c12cab51ed`  
		Last Modified: Fri, 11 Jul 2025 23:33:54 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.8` - unknown; unknown

```console
$ docker pull percona@sha256:3fff02cacad185d53949367226152f1a8d51e1e6fd8791a277cba51e77b9cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ef0c46496d90e0e3ceb18a1672191ac176a4ad8c5333b2aa3dddd189edfae5`

```dockerfile
```

-	Layers:
	-	`sha256:d5147d83cbd03ee45eef34427467bbfb0f7c7e78d9bc3d75348a783b4dd8598c`  
		Last Modified: Sat, 12 Jul 2025 02:10:40 GMT  
		Size: 32.4 KB (32437 bytes)  
		MIME: application/vnd.in-toto+json
