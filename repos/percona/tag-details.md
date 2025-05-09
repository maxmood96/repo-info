<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.41-32`](#percona8041-32)
-	[`percona:8.0.41-32-centos`](#percona8041-32-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.41-32`](#perconaps-8041-32)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.21`](#perconapsmdb-6021)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.16`](#perconapsmdb-7016)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.4`](#perconapsmdb-804)

## `percona:8`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32-centos`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32-centos` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32-centos` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.41-32`

```console
$ docker pull percona@sha256:430156f059298825eacfd85c08497cdd73c4b7bc7c620f51e5a53ba8bd5018b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:c01fc6c752c60bb8195ada972d8e467bc066afc9b3c5e47db7ee2e05c31b8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360996081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9b9a13da8402507c3ac7acd7385fb5133447c1cd91f0d83174ab09b4c9795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec7df0dd86759a618e38ed1307bc95cd4576d4f16b8c85bf82776dfa9f0a5d`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3b26c6e05db2f1353e0cee118c6564818d386338a005c4a1e5243f7698ca6`  
		Last Modified: Thu, 08 May 2025 17:06:36 GMT  
		Size: 8.6 MB (8629285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a9327f219892c6a9236679b2be6f1eea12759d3e4d193b9cfd73966f83a89`  
		Last Modified: Thu, 08 May 2025 17:21:07 GMT  
		Size: 312.6 MB (312642509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa4b9c0f833bf90e986ff5448bd1fb9064b4df4fb097ea6f737e9212e238a7`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0235cdc31a6ff865ccc13d38fb2d27039a33e7e48bb7a148b14747b318e3bd68`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c20273d69ec6cc2b70cb9842bf35afb9d4a8c786cfa3fc25bf666dbfcfd1b`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:66f6eecb047ff8e9b9d7f13124b1f7c575d498d1d730d5dfe980f0427f57151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952766049f03ec09f8157eb4a883c5f06e066e4951d650e16bf13e3c6d77341a`

```dockerfile
```

-	Layers:
	-	`sha256:0e233a5fbf702b9a7cd728df30992d6a80c5b8f2a2cf0e413ab02a6ff02da9a4`  
		Last Modified: Tue, 29 Apr 2025 16:40:11 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:272244a8812620164353fc48522675fe3c1b592dac3562976fe32a242131fd24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:fcce620eea7298bd6ea0a7a2d1246ed132f525022bd64318a758dd499dd309b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253559938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137b65cd1b44419837b52b6d724d27a8aa1e4c8e0225f874c90312cbd3e4174`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdd4b515582be4470b4c92c8dc9eabddcbf672a81bf1fbb95d63b5c031f769`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 8.3 MB (8254711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94e7d886284e720222964efd89258990613bc39b982912ed189cce55e1781a2`  
		Last Modified: Tue, 29 Apr 2025 16:39:43 GMT  
		Size: 204.6 MB (204637860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07728f6bfe1e57f344a37646c8942b5c75d3257a20d929f69d46bf0e5ef76216`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885749c49f1578ccb5d98b15a4020c2e2187c8b2d5976b78b21b0cff3ba56dee`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbbd166ec9f9fee536e86d1cc09cc4e5cba830d29a183e5b4a5f8bbeaf832ae`  
		Last Modified: Fri, 09 May 2025 01:03:16 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528a873dae79705f288001eb60ed7014aa6dc885422557324a9c3d6a37fe8bef`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157aba6a899cc88241ddc98cd39f6479ee2663b639c0c5e8edb3842af2fca95f`  
		Last Modified: Fri, 09 May 2025 01:03:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c652055e0e9aef76615e399e1839dd6fc74a3ea2d75bd42af7316c3a810f9`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:92ec4fa55392d86301324f18eb7d6f340a56648e6f0061e751f4e5925eab9c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac232d273933935d1f55b430228387ab2db2b5324bb4432bbf395e41a2759f`

```dockerfile
```

-	Layers:
	-	`sha256:e727dd9c8e4d1a5679d6ec284a04646a557c60bec7be07f356b57762e60a1ca3`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 33.2 KB (33240 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.21`

```console
$ docker pull percona@sha256:272244a8812620164353fc48522675fe3c1b592dac3562976fe32a242131fd24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.21` - linux; amd64

```console
$ docker pull percona@sha256:fcce620eea7298bd6ea0a7a2d1246ed132f525022bd64318a758dd499dd309b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253559938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137b65cd1b44419837b52b6d724d27a8aa1e4c8e0225f874c90312cbd3e4174`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdd4b515582be4470b4c92c8dc9eabddcbf672a81bf1fbb95d63b5c031f769`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 8.3 MB (8254711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94e7d886284e720222964efd89258990613bc39b982912ed189cce55e1781a2`  
		Last Modified: Tue, 29 Apr 2025 16:39:43 GMT  
		Size: 204.6 MB (204637860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07728f6bfe1e57f344a37646c8942b5c75d3257a20d929f69d46bf0e5ef76216`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885749c49f1578ccb5d98b15a4020c2e2187c8b2d5976b78b21b0cff3ba56dee`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbbd166ec9f9fee536e86d1cc09cc4e5cba830d29a183e5b4a5f8bbeaf832ae`  
		Last Modified: Fri, 09 May 2025 01:03:16 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528a873dae79705f288001eb60ed7014aa6dc885422557324a9c3d6a37fe8bef`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157aba6a899cc88241ddc98cd39f6479ee2663b639c0c5e8edb3842af2fca95f`  
		Last Modified: Fri, 09 May 2025 01:03:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c652055e0e9aef76615e399e1839dd6fc74a3ea2d75bd42af7316c3a810f9`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.21` - unknown; unknown

```console
$ docker pull percona@sha256:92ec4fa55392d86301324f18eb7d6f340a56648e6f0061e751f4e5925eab9c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac232d273933935d1f55b430228387ab2db2b5324bb4432bbf395e41a2759f`

```dockerfile
```

-	Layers:
	-	`sha256:e727dd9c8e4d1a5679d6ec284a04646a557c60bec7be07f356b57762e60a1ca3`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 33.2 KB (33240 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:678e2e6c8e4a5c42c22e8203c762155d388d76da5787f85231b0a13b4612c0a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:35d73413e62686def266438110c5cfc0f64e89a2e0a994e12c92e854fc18594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260867742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f1b58171ef5ee0325fc26b92a3bc20e7ee663855217619237213dfb5a123e4`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=7.0.16-10
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=7.0.16-10.el9
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
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -O https://download.rockylinux.org/pub/rocky/RPM-GPG-KEY-Rocky-9;     rpm --import RPM-GPG-KEY-Rocky-9;     curl -Lf -o /tmp/numactl.rpm https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/n/numactl-2.0.18-2.${OS_VER}.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd70fcfa1ac653940b9acb696401b4728596b5e540182a6d910acb36764ef17`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 8.3 MB (8251350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b1dfb8917c54ad2495693c509ddcdba131f549e712ec753bec20b00a0735b`  
		Last Modified: Tue, 29 Apr 2025 16:39:43 GMT  
		Size: 211.9 MB (211949012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3fa93ad25e49a8b38135538e79d0804d8e4cbb0e481d37a888342173d5d628`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885749c49f1578ccb5d98b15a4020c2e2187c8b2d5976b78b21b0cff3ba56dee`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a549e2701872cc1e053250852e333cbd2234c8ad2cf53a2e5df495e7611be9`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528a873dae79705f288001eb60ed7014aa6dc885422557324a9c3d6a37fe8bef`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228114d07adab23ca87f0a6b7f91b7871112acd1012d23c5b22bd88b9f90b4c`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69337a0ae4761ecab802e5fb1213177c670b3df1e4a57685cf35f746a5ad9b7`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 4.8 KB (4828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:08faa7deff0a52a34559e071235638d333ff6c487791dcd25c4e62bedd3ad960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d166c0d13573517dcaf0883e351b7285295cc682a72f809502583447f5383208`

```dockerfile
```

-	Layers:
	-	`sha256:62f24a4f8e8c03c005298485a626aad133c018ebe48c7c30d3707bbee5110149`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 33.1 KB (33105 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.16`

```console
$ docker pull percona@sha256:678e2e6c8e4a5c42c22e8203c762155d388d76da5787f85231b0a13b4612c0a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.16` - linux; amd64

```console
$ docker pull percona@sha256:35d73413e62686def266438110c5cfc0f64e89a2e0a994e12c92e854fc18594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260867742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f1b58171ef5ee0325fc26b92a3bc20e7ee663855217619237213dfb5a123e4`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=7.0.16-10
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=7.0.16-10.el9
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
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -O https://download.rockylinux.org/pub/rocky/RPM-GPG-KEY-Rocky-9;     rpm --import RPM-GPG-KEY-Rocky-9;     curl -Lf -o /tmp/numactl.rpm https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/n/numactl-2.0.18-2.${OS_VER}.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd70fcfa1ac653940b9acb696401b4728596b5e540182a6d910acb36764ef17`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 8.3 MB (8251350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b1dfb8917c54ad2495693c509ddcdba131f549e712ec753bec20b00a0735b`  
		Last Modified: Tue, 29 Apr 2025 16:39:43 GMT  
		Size: 211.9 MB (211949012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3fa93ad25e49a8b38135538e79d0804d8e4cbb0e481d37a888342173d5d628`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885749c49f1578ccb5d98b15a4020c2e2187c8b2d5976b78b21b0cff3ba56dee`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a549e2701872cc1e053250852e333cbd2234c8ad2cf53a2e5df495e7611be9`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528a873dae79705f288001eb60ed7014aa6dc885422557324a9c3d6a37fe8bef`  
		Last Modified: Fri, 09 May 2025 01:03:15 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228114d07adab23ca87f0a6b7f91b7871112acd1012d23c5b22bd88b9f90b4c`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69337a0ae4761ecab802e5fb1213177c670b3df1e4a57685cf35f746a5ad9b7`  
		Last Modified: Fri, 09 May 2025 02:23:28 GMT  
		Size: 4.8 KB (4828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.16` - unknown; unknown

```console
$ docker pull percona@sha256:08faa7deff0a52a34559e071235638d333ff6c487791dcd25c4e62bedd3ad960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d166c0d13573517dcaf0883e351b7285295cc682a72f809502583447f5383208`

```dockerfile
```

-	Layers:
	-	`sha256:62f24a4f8e8c03c005298485a626aad133c018ebe48c7c30d3707bbee5110149`  
		Last Modified: Tue, 29 Apr 2025 16:39:40 GMT  
		Size: 33.1 KB (33105 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:b6886ec678988ea0fff71c2071d184591117a797d9495986ffeca57e47bbb41e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:90278db316036d29918f3e8af62d700783160ab5582a9a018364b06da829ac76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277799109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee99b1665dde67c8238254510b8b366323fec16232156e58efca8527e1e95b36`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=8.0.4-2
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=8.0.4-2.el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_REPO=testing
# Tue, 22 Apr 2025 10:21:47 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 22 Apr 2025 10:21:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -O https://download.rockylinux.org/pub/rocky/RPM-GPG-KEY-Rocky-9;     rpm --import RPM-GPG-KEY-Rocky-9;     curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -Lf -o /tmp/numactl.rpm https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/n/numactl-2.0.18-2.${OS_VER}.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20557b9bf0de1adad1a7db947c99a0edbd032679efa45a86610adb06e2692`  
		Last Modified: Thu, 08 May 2025 17:35:50 GMT  
		Size: 8.3 MB (8251406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9998c57248150b7c746b8d685f14f3e46c37526b36f04b1b69938c89823d18`  
		Last Modified: Thu, 08 May 2025 17:48:05 GMT  
		Size: 228.9 MB (228880329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd615b67525a7eac28d86395e3c2164788bcd5b3486f844f1b063bd947e20f2`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8546c7f3121d8f338db80948d1b3c95e63985fb23094837a960f337ed42d5c51`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5532e09f642dbe65ab54f883bac6bae9b5b814bfc5ed982e81a854788200a0`  
		Last Modified: Thu, 08 May 2025 17:35:49 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e802c8d3578e6ea65d21f098cdc74380e2934b1123c73a612b05a5865e0f3cf`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b389e9df6e17a608448280667902f03beb56124edc621d98f2d8c931bc51b76`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa455c70a0e7064b1d4d6d3fe628d882114fc2a395c1973166f635d4f6963d9`  
		Last Modified: Thu, 08 May 2025 17:35:49 GMT  
		Size: 4.8 KB (4823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:7a7839f3e5e0c2f85f0b080818711fab78530125f3c54340c0b7424431245e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1b16ed157e14422b5635eaca7a4d7a1611a6d592fb21a6281fa032bec3b351`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ee759c31ed9821d85d5536f23ac2618d6d5bd50d9e1aad70be9c2ac6d14fa`  
		Last Modified: Tue, 29 Apr 2025 16:39:47 GMT  
		Size: 33.4 KB (33377 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.4`

```console
$ docker pull percona@sha256:b6886ec678988ea0fff71c2071d184591117a797d9495986ffeca57e47bbb41e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.4` - linux; amd64

```console
$ docker pull percona@sha256:90278db316036d29918f3e8af62d700783160ab5582a9a018364b06da829ac76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277799109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee99b1665dde67c8238254510b8b366323fec16232156e58efca8527e1e95b36`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=8.0.4-2
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=8.0.4-2.el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_REPO=testing
# Tue, 22 Apr 2025 10:21:47 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 22 Apr 2025 10:21:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -O https://download.rockylinux.org/pub/rocky/RPM-GPG-KEY-Rocky-9;     rpm --import RPM-GPG-KEY-Rocky-9;     curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -Lf -o /tmp/numactl.rpm https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/n/numactl-2.0.18-2.${OS_VER}.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20557b9bf0de1adad1a7db947c99a0edbd032679efa45a86610adb06e2692`  
		Last Modified: Thu, 08 May 2025 17:35:50 GMT  
		Size: 8.3 MB (8251406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9998c57248150b7c746b8d685f14f3e46c37526b36f04b1b69938c89823d18`  
		Last Modified: Thu, 08 May 2025 17:48:05 GMT  
		Size: 228.9 MB (228880329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd615b67525a7eac28d86395e3c2164788bcd5b3486f844f1b063bd947e20f2`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8546c7f3121d8f338db80948d1b3c95e63985fb23094837a960f337ed42d5c51`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a7b2df76e10d229d43c1671b8c5120a2e8aad0988ed49af44d3ab5b1309675`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5532e09f642dbe65ab54f883bac6bae9b5b814bfc5ed982e81a854788200a0`  
		Last Modified: Thu, 08 May 2025 17:35:49 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e802c8d3578e6ea65d21f098cdc74380e2934b1123c73a612b05a5865e0f3cf`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b389e9df6e17a608448280667902f03beb56124edc621d98f2d8c931bc51b76`  
		Last Modified: Thu, 08 May 2025 17:35:48 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa455c70a0e7064b1d4d6d3fe628d882114fc2a395c1973166f635d4f6963d9`  
		Last Modified: Thu, 08 May 2025 17:35:49 GMT  
		Size: 4.8 KB (4823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.4` - unknown; unknown

```console
$ docker pull percona@sha256:7a7839f3e5e0c2f85f0b080818711fab78530125f3c54340c0b7424431245e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1b16ed157e14422b5635eaca7a4d7a1611a6d592fb21a6281fa032bec3b351`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ee759c31ed9821d85d5536f23ac2618d6d5bd50d9e1aad70be9c2ac6d14fa`  
		Last Modified: Tue, 29 Apr 2025 16:39:47 GMT  
		Size: 33.4 KB (33377 bytes)  
		MIME: application/vnd.in-toto+json
