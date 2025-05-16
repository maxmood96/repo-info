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
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32-centos`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32-centos` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32-centos` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.41-32`

```console
$ docker pull percona@sha256:9930302c412b473d01060124c38b4f48c460d673a54e7e63794f5183e4a133ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:86eb398b6210a0c592155f30b1b94a7b3e62002f6ca97fce6e81a2556b620301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361167081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55e884677ba602c96ad853c028a61968ca8c907e1d6c19d54b4de54ad4b9e5`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cc7e1e4cfb93cb4a8b0938311e6898cd49a1dec3c22ade65da2ff6b1c18f9`  
		Last Modified: Thu, 15 May 2025 19:27:15 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e8d22b7592e9122fd47e8bce49e52a12ffb672b7029264cca602303567fb0`  
		Last Modified: Thu, 15 May 2025 19:27:17 GMT  
		Size: 8.9 MB (8853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0753058a0484b953d8a8b2d2cc244f23a2d418a840dc53fca9789891d6e38`  
		Last Modified: Thu, 15 May 2025 19:27:42 GMT  
		Size: 312.7 MB (312658254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f08286539c5507c9885e94a287f75f4cd95fa3d1fca682f73d3ecea5e21854`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb4ed0b791cec82a8e1e1510425aacd42e7cd4ba3fe6765f4dfbc6eba10940`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd138c99504cdb2a7e78c4e8d0d469a78457ae5dbc88463037f0923cb53db21`  
		Last Modified: Thu, 15 May 2025 19:27:16 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:d1ba67d14cc640607a6ff0195e436a250f79616c85bc7c0d71173087ece3df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0183ad1edf802037555b4a582298d2ab56fcb1b8c9ef47dbe64991adcc40e`

```dockerfile
```

-	Layers:
	-	`sha256:41b1b8dde23db10a0bf644fca59da1ae9d0834173375a4cc730eeab1ee6a573e`  
		Last Modified: Wed, 14 May 2025 23:48:59 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:a2cc97c29ccb16b282edf46b1e35dc8b4d83504172cc7256f3b2747bed4da0d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:a906824d2b413bcafda1fadc1d3cd9c0895b23619dfc327d7987560aa456a650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253729792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd2dcb48a29365f3728058f0a5a0a2ab561bd29913908532e70871c6c48166b`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c708ebf381e053feb6862e11992671d3eba4610efda6de5c3632c4d0df1b8`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 8.5 MB (8482467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841faea2c3001ba2c6651a1471d40ba85f3843dd55a76dc5b2a7d040a651930b`  
		Last Modified: Wed, 14 May 2025 23:48:51 GMT  
		Size: 204.6 MB (204649415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eb23f07344e6e475d56549ff8d7cec7dbe70b484e16831a493f19e38429ece`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a86b510fd19b254bbe1fbf90f6276c24c7420a9b0cee0bd97482533538aaf7`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b467af7a66519ddf840fcc8bc7eac4ccdb10e0dbcb65369175cfc0c84c4d0b`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848c8ad0fd4069b74a370c2de7eaaa84bba007a7372a39585c673a8c6d80482`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bee0ed0592412fecc5fb0f98a0817c2dc55463e6aaf7a2871d5bacaafa2b55`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d64021ebdc2451d656ff8691ba878eb4a43065a6747fa34ea56df4653f89b85`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d71bdf0d07cbcb3e68b943a8d05872b9c3af5f24f5ce932d8d3b19746fa62c`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:474e49e01add4c91abc44ba3117e0910384a0d39e14be1600ff56f55942a316f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5e0f9f5f23f481f4bca9fbf776759cc31fac84bd03a79087e89a8d9ef194e`

```dockerfile
```

-	Layers:
	-	`sha256:f04b3a606033856eb3dae070274f77e19082c23ca55bcb0de8dbcc2f6529dddd`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.21`

```console
$ docker pull percona@sha256:a2cc97c29ccb16b282edf46b1e35dc8b4d83504172cc7256f3b2747bed4da0d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.21` - linux; amd64

```console
$ docker pull percona@sha256:a906824d2b413bcafda1fadc1d3cd9c0895b23619dfc327d7987560aa456a650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253729792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd2dcb48a29365f3728058f0a5a0a2ab561bd29913908532e70871c6c48166b`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c708ebf381e053feb6862e11992671d3eba4610efda6de5c3632c4d0df1b8`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 8.5 MB (8482467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841faea2c3001ba2c6651a1471d40ba85f3843dd55a76dc5b2a7d040a651930b`  
		Last Modified: Wed, 14 May 2025 23:48:51 GMT  
		Size: 204.6 MB (204649415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eb23f07344e6e475d56549ff8d7cec7dbe70b484e16831a493f19e38429ece`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a86b510fd19b254bbe1fbf90f6276c24c7420a9b0cee0bd97482533538aaf7`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b467af7a66519ddf840fcc8bc7eac4ccdb10e0dbcb65369175cfc0c84c4d0b`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848c8ad0fd4069b74a370c2de7eaaa84bba007a7372a39585c673a8c6d80482`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bee0ed0592412fecc5fb0f98a0817c2dc55463e6aaf7a2871d5bacaafa2b55`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d64021ebdc2451d656ff8691ba878eb4a43065a6747fa34ea56df4653f89b85`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d71bdf0d07cbcb3e68b943a8d05872b9c3af5f24f5ce932d8d3b19746fa62c`  
		Last Modified: Fri, 16 May 2025 16:21:51 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.21` - unknown; unknown

```console
$ docker pull percona@sha256:474e49e01add4c91abc44ba3117e0910384a0d39e14be1600ff56f55942a316f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5e0f9f5f23f481f4bca9fbf776759cc31fac84bd03a79087e89a8d9ef194e`

```dockerfile
```

-	Layers:
	-	`sha256:f04b3a606033856eb3dae070274f77e19082c23ca55bcb0de8dbcc2f6529dddd`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:e9e89d299f2ce383c70277a4847b76c465fe5643487e75f09ed834452a002fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:24011b689fa2ee4a21579af292956e097aff0ec26a17ec5b38c8f82c196ec77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261045852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51144923bb8a934d3a5b9b9e4849f98f304c2136f605ebe34988f2e8d20539a`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94da69da44f38163581b1723402f2aae99f46cba2827ce4a78d3fbfcba42d34`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 8.5 MB (8477903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cfee4a9561a029fe2492ecd55d68c434058c58ec499ba5d09fc0367c1260c5`  
		Last Modified: Wed, 14 May 2025 23:48:50 GMT  
		Size: 212.0 MB (211970025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d0d1dcb41538363667e7426ce1eda0a768d6d88f401afb26b20dfdd606a0d`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc25ade0ee4fef7ee2a64c99b6e02c2827296fa0e034e4008595790c5e8278`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ad5fa8511211562d3c129413df0e30446ddce59a60a35a5e9bf27d300f8dcf`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d5788b05f8e49a45eb1dc43f1e1743dda13467ddcc7af317a19c70cfa4f4f4`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb842c05682ae200455927734e2e335820663701b9ac4672dcfa34a19689151`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7932ea5adf18155dcd22ede091e66cdbd55f097e87762352ebcf90355e3d4`  
		Last Modified: Wed, 14 May 2025 23:48:49 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cca5176cd784e783af1909761a0f3d83b97379abb7ec21c8c5604931dce9fb`  
		Last Modified: Wed, 14 May 2025 23:48:49 GMT  
		Size: 4.8 KB (4829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:163935426bc2f2864d4c7e6333b98029d731f3347bf8a913f2342fbcadf4c81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283d1881dab82491028019356d54bc30976be77159515ea1b0b86c3a81eaeb65`

```dockerfile
```

-	Layers:
	-	`sha256:eba9de8e040193d58717d3b3b09b80fb15f34e36bac075655d7f7274d6840444`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 33.1 KB (33105 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.16`

```console
$ docker pull percona@sha256:e9e89d299f2ce383c70277a4847b76c465fe5643487e75f09ed834452a002fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.16` - linux; amd64

```console
$ docker pull percona@sha256:24011b689fa2ee4a21579af292956e097aff0ec26a17ec5b38c8f82c196ec77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261045852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51144923bb8a934d3a5b9b9e4849f98f304c2136f605ebe34988f2e8d20539a`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94da69da44f38163581b1723402f2aae99f46cba2827ce4a78d3fbfcba42d34`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 8.5 MB (8477903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cfee4a9561a029fe2492ecd55d68c434058c58ec499ba5d09fc0367c1260c5`  
		Last Modified: Wed, 14 May 2025 23:48:50 GMT  
		Size: 212.0 MB (211970025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d0d1dcb41538363667e7426ce1eda0a768d6d88f401afb26b20dfdd606a0d`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc25ade0ee4fef7ee2a64c99b6e02c2827296fa0e034e4008595790c5e8278`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ad5fa8511211562d3c129413df0e30446ddce59a60a35a5e9bf27d300f8dcf`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d5788b05f8e49a45eb1dc43f1e1743dda13467ddcc7af317a19c70cfa4f4f4`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb842c05682ae200455927734e2e335820663701b9ac4672dcfa34a19689151`  
		Last Modified: Wed, 14 May 2025 23:48:48 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7932ea5adf18155dcd22ede091e66cdbd55f097e87762352ebcf90355e3d4`  
		Last Modified: Wed, 14 May 2025 23:48:49 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cca5176cd784e783af1909761a0f3d83b97379abb7ec21c8c5604931dce9fb`  
		Last Modified: Wed, 14 May 2025 23:48:49 GMT  
		Size: 4.8 KB (4829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.16` - unknown; unknown

```console
$ docker pull percona@sha256:163935426bc2f2864d4c7e6333b98029d731f3347bf8a913f2342fbcadf4c81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283d1881dab82491028019356d54bc30976be77159515ea1b0b86c3a81eaeb65`

```dockerfile
```

-	Layers:
	-	`sha256:eba9de8e040193d58717d3b3b09b80fb15f34e36bac075655d7f7274d6840444`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 33.1 KB (33105 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:2b0f6393c73dc92175365e411d31d38c7b4bcca992ea87f059a8d3f2049cf5bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:1dff70fa617ad5546cbea3e68f71c620047c5e97d47e2a950bda38287d2ca75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277969918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad922c7f38eb1cd68929eaf24f26261a83a5cb715143720e11cd055d5b829ca`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d801372fe6ebce610862fe2c37dbfa227c7d34e491abf541f48873251a447f`  
		Last Modified: Fri, 16 May 2025 17:41:43 GMT  
		Size: 8.5 MB (8477868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c10f8cdc7f8866956b83df4962da7eea5e87e56d8dc368b27b7649cf86e6edb`  
		Last Modified: Fri, 16 May 2025 17:43:22 GMT  
		Size: 228.9 MB (228894135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fe33ab33148b0252d114b94aba4ca4370fd684657dbcd9be7ae7b0d6aecf01`  
		Last Modified: Fri, 16 May 2025 17:41:46 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2397073a0237bdb0b7dff13dfb95fc552ec4333dd3ffa9867f792ec897410`  
		Last Modified: Fri, 16 May 2025 17:41:46 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0437180f7960373908bdb1b05ba03c3ef4538de649d8c4f10008de750d6006a9`  
		Last Modified: Fri, 16 May 2025 17:41:47 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e8afd6720fe31a7465500dd96d849b40fb13d7bbf2fdcde25b9b3b1d5ab591`  
		Last Modified: Fri, 16 May 2025 17:41:48 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6f00e472661afa69c416454bc4a47bb8036d1b3b416552f8cce25a43c598c`  
		Last Modified: Fri, 16 May 2025 17:41:50 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922399769d22f51b3c5d65a93fc597e538c44808cad7752178a7d59c80d07c8`  
		Last Modified: Fri, 16 May 2025 17:41:50 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e727eab2a145496d4d4d91aa8e74d1598bae45cbbe79e4addca636cdba893d`  
		Last Modified: Fri, 16 May 2025 17:41:53 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:8e1ef1f5dbab3f06b0d635c92484fe89d9edaa41d3cb80f64f9c8130920898b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259d6a0d0d240be8176dbd989fdfeabed4ff285963c212ca2649ab734a7c1344`

```dockerfile
```

-	Layers:
	-	`sha256:15e69a180bbaaefabab41d94dd07962b4adaf5200bf73ff1f03573ae3d3fcbe5`  
		Last Modified: Wed, 14 May 2025 23:48:43 GMT  
		Size: 33.4 KB (33376 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.4`

```console
$ docker pull percona@sha256:2b0f6393c73dc92175365e411d31d38c7b4bcca992ea87f059a8d3f2049cf5bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.4` - linux; amd64

```console
$ docker pull percona@sha256:1dff70fa617ad5546cbea3e68f71c620047c5e97d47e2a950bda38287d2ca75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277969918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad922c7f38eb1cd68929eaf24f26261a83a5cb715143720e11cd055d5b829ca`
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d801372fe6ebce610862fe2c37dbfa227c7d34e491abf541f48873251a447f`  
		Last Modified: Fri, 16 May 2025 17:41:43 GMT  
		Size: 8.5 MB (8477868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c10f8cdc7f8866956b83df4962da7eea5e87e56d8dc368b27b7649cf86e6edb`  
		Last Modified: Fri, 16 May 2025 17:43:22 GMT  
		Size: 228.9 MB (228894135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fe33ab33148b0252d114b94aba4ca4370fd684657dbcd9be7ae7b0d6aecf01`  
		Last Modified: Fri, 16 May 2025 17:41:46 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2397073a0237bdb0b7dff13dfb95fc552ec4333dd3ffa9867f792ec897410`  
		Last Modified: Fri, 16 May 2025 17:41:46 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0437180f7960373908bdb1b05ba03c3ef4538de649d8c4f10008de750d6006a9`  
		Last Modified: Fri, 16 May 2025 17:41:47 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e8afd6720fe31a7465500dd96d849b40fb13d7bbf2fdcde25b9b3b1d5ab591`  
		Last Modified: Fri, 16 May 2025 17:41:48 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6f00e472661afa69c416454bc4a47bb8036d1b3b416552f8cce25a43c598c`  
		Last Modified: Fri, 16 May 2025 17:41:50 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922399769d22f51b3c5d65a93fc597e538c44808cad7752178a7d59c80d07c8`  
		Last Modified: Fri, 16 May 2025 17:41:50 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e727eab2a145496d4d4d91aa8e74d1598bae45cbbe79e4addca636cdba893d`  
		Last Modified: Fri, 16 May 2025 17:41:53 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.4` - unknown; unknown

```console
$ docker pull percona@sha256:8e1ef1f5dbab3f06b0d635c92484fe89d9edaa41d3cb80f64f9c8130920898b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259d6a0d0d240be8176dbd989fdfeabed4ff285963c212ca2649ab734a7c1344`

```dockerfile
```

-	Layers:
	-	`sha256:15e69a180bbaaefabab41d94dd07962b4adaf5200bf73ff1f03573ae3d3fcbe5`  
		Last Modified: Wed, 14 May 2025 23:48:43 GMT  
		Size: 33.4 KB (33376 bytes)  
		MIME: application/vnd.in-toto+json
