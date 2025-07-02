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
-	[`percona:psmdb-6.0.21`](#perconapsmdb-6021)

## `percona:8`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.42-33`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.42-33` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.42-33` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.42-33-centos`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.42-33-centos` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.42-33-centos` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.42-33`

```console
$ docker pull percona@sha256:bd6a129570fbeeab01a000d7a01235745f9ba968ea57528883171ff690c9725b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.42-33` - linux; amd64

```console
$ docker pull percona@sha256:49b94577c4bbe2a7bdf01f37ecf816568bef072edfb375588a6f11f7fa16c568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431013622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906c36d46106f3340f4aa4f20261a29fa9fcc6c0956fe920848ae880d629cce`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833c4f48e915e02793f077b653e12adfaf6fb04bf71ea1d7b81bc2423a3b41`  
		Last Modified: Wed, 02 Jul 2025 18:45:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6df8b8e9ce7106992277ec95a6fd120201247fcc0d12fcf2232fd93c28150`  
		Last Modified: Wed, 02 Jul 2025 18:45:40 GMT  
		Size: 8.8 MB (8846323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7d8e0bb9e2fff3fa66e7b28736c3978b5100ce0af268471b552ab1803e2d0`  
		Last Modified: Wed, 02 Jul 2025 20:10:34 GMT  
		Size: 382.5 MB (382506739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5e62aef268cc39084403432cd1a117aa4eca05596b2b8ded7e3716bcb7118`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c2d11ba398ee5009c1c0f05fa2806c7fd765be290dc0c756ee5cac0e5d1a5`  
		Last Modified: Wed, 02 Jul 2025 18:45:34 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3841a31d366f9addf867001f6cdaf44552ff99e304b3c698bfc6c54e1dd0`  
		Last Modified: Wed, 02 Jul 2025 18:45:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.42-33` - unknown; unknown

```console
$ docker pull percona@sha256:46ca114fc408794159e3a439c0e62d77b621051ce5c01d9e28750acbc39cef90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79bf11d17201adeeb909b6d620d8f3fac5b79eefbc8f17a6940a3ab57fdc4f`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e67acbf836653a39c833b1a3c5d818df1c3fbf9dfd49136c57b19f604578f`  
		Last Modified: Wed, 02 Jul 2025 20:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:7af22227abceabf785ffef7709138aaa6de040c944e5a9817fd8151de66b70fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:766ff036661ec878c87335cabdc7bd7d62c6e4de49d07e9bd763e32e686457c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254039353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cb2e601f575e0b16994ca3d24a92af9cd705353b7638ca5b8ed4e50f35408e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL url="https://www.redhat.com"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 22 Apr 2025 10:21:47 GMT
ENV container oci
# Tue, 22 Apr 2025 10:21:47 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=6.0.21-18
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=6.0.21-18.el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_REPO=release
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 22 Apr 2025 10:21:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -Lf -o /tmp/numactl.rpm https://yum.oracle.com/repo/OracleLinux/OL9/baseos/latest/x86_64/getPackage/numactl-2.0.16-1.el9.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV GOSU_VERSION=1.11
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
VOLUME [/data/db]
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 22 Apr 2025 10:21:47 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Apr 2025 10:21:47 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 22 Apr 2025 10:21:47 GMT
USER 1001
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519acb5a08231668bb8175e85709764d835a69aa2285b7adeb544690b2610b16`  
		Last Modified: Wed, 02 Jul 2025 18:45:10 GMT  
		Size: 8.5 MB (8476027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415f1d92ec2a451f97dd0ab59cfa3683b8727ac0ddd65839e1a43dc8961d9e9`  
		Last Modified: Wed, 02 Jul 2025 20:10:47 GMT  
		Size: 205.0 MB (204959681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0532507a2617177b2323fb9de91cae85ead7a8fd69f020777c31dc762bc601`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f623e0fbc0b3c109715412a65b9ce6498feaa1c599f52c2097216aceb3999`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ca71d147767aae845c216a7c53ff9e1cb45abb8f00b0706633ed9c68cc5aa2`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63a895670800ae859ef761585e8e946982d6fe3c5447ab1fb26e0c94b2908d`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d64723267e2a4cba1d3afa76b9241d65a657301ecc8594a21902defad81ab9`  
		Last Modified: Wed, 02 Jul 2025 18:45:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096097c37731040133c5a8886899ce2403c93726b865212bb4adc6d8182cbb93`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87057e0b6e390378a567f753f6e45f58b6a8fd5aaeebbf4bcd76f27135c597ef`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 4.8 KB (4827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:bfc433096d9e60fb90254e2bc224bf82c968569ccd1f765faa4f5cc13d80f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d36d77dad66963633b8bb67278abf3b95194b07f5ab6678f4ac4bc66c1c1a`

```dockerfile
```

-	Layers:
	-	`sha256:d9026c27858dabf524fd7990af76eb229ed3bf0e361854d0c708efbb7d5a9b65`  
		Last Modified: Wed, 02 Jul 2025 20:10:28 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.21`

```console
$ docker pull percona@sha256:7af22227abceabf785ffef7709138aaa6de040c944e5a9817fd8151de66b70fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.21` - linux; amd64

```console
$ docker pull percona@sha256:766ff036661ec878c87335cabdc7bd7d62c6e4de49d07e9bd763e32e686457c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254039353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cb2e601f575e0b16994ca3d24a92af9cd705353b7638ca5b8ed4e50f35408e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL url="https://www.redhat.com"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 22 Apr 2025 10:21:47 GMT
ENV container oci
# Tue, 22 Apr 2025 10:21:47 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=6.0.21-18
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=6.0.21-18.el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_REPO=release
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 22 Apr 2025 10:21:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -Lf -o /tmp/numactl.rpm https://yum.oracle.com/repo/OracleLinux/OL9/baseos/latest/x86_64/getPackage/numactl-2.0.16-1.el9.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV GOSU_VERSION=1.11
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
VOLUME [/data/db]
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 22 Apr 2025 10:21:47 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Apr 2025 10:21:47 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 22 Apr 2025 10:21:47 GMT
USER 1001
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519acb5a08231668bb8175e85709764d835a69aa2285b7adeb544690b2610b16`  
		Last Modified: Wed, 02 Jul 2025 18:45:10 GMT  
		Size: 8.5 MB (8476027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415f1d92ec2a451f97dd0ab59cfa3683b8727ac0ddd65839e1a43dc8961d9e9`  
		Last Modified: Wed, 02 Jul 2025 20:10:47 GMT  
		Size: 205.0 MB (204959681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0532507a2617177b2323fb9de91cae85ead7a8fd69f020777c31dc762bc601`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f623e0fbc0b3c109715412a65b9ce6498feaa1c599f52c2097216aceb3999`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ca71d147767aae845c216a7c53ff9e1cb45abb8f00b0706633ed9c68cc5aa2`  
		Last Modified: Wed, 02 Jul 2025 18:45:07 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63a895670800ae859ef761585e8e946982d6fe3c5447ab1fb26e0c94b2908d`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d64723267e2a4cba1d3afa76b9241d65a657301ecc8594a21902defad81ab9`  
		Last Modified: Wed, 02 Jul 2025 18:45:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096097c37731040133c5a8886899ce2403c93726b865212bb4adc6d8182cbb93`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87057e0b6e390378a567f753f6e45f58b6a8fd5aaeebbf4bcd76f27135c597ef`  
		Last Modified: Wed, 02 Jul 2025 18:45:09 GMT  
		Size: 4.8 KB (4827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.21` - unknown; unknown

```console
$ docker pull percona@sha256:bfc433096d9e60fb90254e2bc224bf82c968569ccd1f765faa4f5cc13d80f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d36d77dad66963633b8bb67278abf3b95194b07f5ab6678f4ac4bc66c1c1a`

```dockerfile
```

-	Layers:
	-	`sha256:d9026c27858dabf524fd7990af76eb229ed3bf0e361854d0c708efbb7d5a9b65`  
		Last Modified: Wed, 02 Jul 2025 20:10:28 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json
