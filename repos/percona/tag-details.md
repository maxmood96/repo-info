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
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.41-32-centos`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.41-32-centos` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.41-32-centos` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.41-32`

```console
$ docker pull percona@sha256:5b3572b6f40077add552683e726389a21b21f50e9c1fc5e83ad33d458fb86f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:02d9c9bb2a1553fba13c1c0db24e4e77db30bc4de168d11438aae1491c62a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228d089ff7839792200beda1d8dc8b94f03a29055ee08c1cfc781c56c92a91`
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
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 18 Feb 2025 16:18:37 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743dbb854f98e2a8ab708ab9cf351dc0ffcd2c20bde5867fcfd3c0ea3a868da`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c67ce6cd3ad60624e89b641acdf6912e7c4a84fa45e377a4175b164ee66b7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 8.3 MB (8309891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b244d29466b8d99f64ec37acf79aa2981d36b7cbc52d72f0ebb5f5f3a76092`  
		Last Modified: Thu, 27 Mar 2025 18:00:12 GMT  
		Size: 312.6 MB (312586064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf263bdb160d01ee4ae4a6dacc912413f1deeee31a311dd8c7e854ab3aab7fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372249fb532fbe208302d54ad37dfc7e7c4ab1dc2fa042ae18372f86abdf2814`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd6516f1875a18b169e155f8bca5beed44fe75e3779cedf13ddbdb22dfa9c2`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:58374df3e8a44c7b5cc283f5fb60e30b0a87ee34cca7c1b1243809d40ac88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8963d9df3949893a9c08b3db7716a9bddab8d16a046ac263bd8f0906addb73`

```dockerfile
```

-	Layers:
	-	`sha256:d9b041b6a5d9d109de59613031c3b39b5c9e6b5c56eeb7912b57fbfe58bfb9d7`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:4bc5edf6a31d9b16fdcb669e522f3698417db97dcfd54edfefb2cf0a059f2099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:80bf81c17f2c749f309f3f95bf29fabbfcdcfd9b52d3daef1a3761a823655c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252703352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13b8956468ef565408c5969d825587857b944d6933d60defe6768e5ad1722cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80494a8c483b7edf542e9dcbcd03571a53546703feef465df1f6bb76044901c5`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 8.0 MB (7958104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d12bdc812fb79b9648b05e4c16e42808add06eaddf6dd0eece6d96e8ccbb7`  
		Last Modified: Tue, 22 Apr 2025 18:32:14 GMT  
		Size: 204.4 MB (204385946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce42b596513fdd235a685e40bf57f96e3cb81f2edad6d8452a6c7c938e34bd8`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806093b6ab4f838e38a9d17a60f1a5d3b1b4bc9503f2d44507ac23fee796c5f3`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dff26afbb4645702c026a2d387ecd3939ca45ba679eb8930febefa4ecd0644`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca178f9b65ea1f68283e5a61ae7d4c45151d14df24eb4d8ad353593f7d4406`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7a11729e94552edf86956c73bf603c39e1079ad2365920dc51e19178cbb93c`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16bbaac031dba235ad465ccbef28a633431490fa82595ba825b2b0adb12d1bc`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdd9081080beffec142b1fea3ca3c529a18e0814b316b1a09f2f061d6b1f3dc`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:785a3ddc168cd42da67f0eed7afa7845ca9568874b0c13ac9a200898a6417f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16e4641780710441622cd4fc98045997c94d5b3f0b7348a159b972562dfc68e`

```dockerfile
```

-	Layers:
	-	`sha256:4e19a224ee8fa2a0a126bdc0309f9a54b38b7e4f6f0544f25001bd43589460a4`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.21`

```console
$ docker pull percona@sha256:4bc5edf6a31d9b16fdcb669e522f3698417db97dcfd54edfefb2cf0a059f2099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.21` - linux; amd64

```console
$ docker pull percona@sha256:80bf81c17f2c749f309f3f95bf29fabbfcdcfd9b52d3daef1a3761a823655c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252703352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13b8956468ef565408c5969d825587857b944d6933d60defe6768e5ad1722cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80494a8c483b7edf542e9dcbcd03571a53546703feef465df1f6bb76044901c5`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 8.0 MB (7958104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d12bdc812fb79b9648b05e4c16e42808add06eaddf6dd0eece6d96e8ccbb7`  
		Last Modified: Tue, 22 Apr 2025 18:32:14 GMT  
		Size: 204.4 MB (204385946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce42b596513fdd235a685e40bf57f96e3cb81f2edad6d8452a6c7c938e34bd8`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806093b6ab4f838e38a9d17a60f1a5d3b1b4bc9503f2d44507ac23fee796c5f3`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dff26afbb4645702c026a2d387ecd3939ca45ba679eb8930febefa4ecd0644`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca178f9b65ea1f68283e5a61ae7d4c45151d14df24eb4d8ad353593f7d4406`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7a11729e94552edf86956c73bf603c39e1079ad2365920dc51e19178cbb93c`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16bbaac031dba235ad465ccbef28a633431490fa82595ba825b2b0adb12d1bc`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdd9081080beffec142b1fea3ca3c529a18e0814b316b1a09f2f061d6b1f3dc`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.21` - unknown; unknown

```console
$ docker pull percona@sha256:785a3ddc168cd42da67f0eed7afa7845ca9568874b0c13ac9a200898a6417f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16e4641780710441622cd4fc98045997c94d5b3f0b7348a159b972562dfc68e`

```dockerfile
```

-	Layers:
	-	`sha256:4e19a224ee8fa2a0a126bdc0309f9a54b38b7e4f6f0544f25001bd43589460a4`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:c02e9bb4bc78fc69b2ec21de36dfabe4de2002ae654a7ed200cfb08447c0449e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:50e298cd551cd71ff803b7393910758ed030bbb42856886c09fb20288144b217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260309885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e06d1950eb8d3d87c5ff69bc83f2df11affd95e9ec39e4b98945269299b0aa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e296324865139a0256e5b0c24c56b13abc0ffbc4187b84d97c16faf4a2ed42`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 8.0 MB (7955244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feff4dd39d2418ebf2c2ee3d6e144890c6bef994dd25990c33cd67d749e376a8`  
		Last Modified: Tue, 22 Apr 2025 18:32:07 GMT  
		Size: 212.0 MB (211995330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492e4641fcd852c3509863d434da0ecc7b3df29bab240071e5b71afa6b43cba`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f1e8594ca8bb14b1131d84ce370d42084e8f4e7cb7099c8a5ab80b30916f2`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f5565eba0829883af857c4e1bfd626499509f78cba7cd51ac373f05928a5fa`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e2b86f95f4cf558bf317db4e1e6523fb38b4cfcd32001906aa46ef56e5a56`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c3b61046ef9fa0a0e2f7187f3a15fefecff5507784d6753ebc3e8323e0a27a`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a85065b015a733f051a6bb00417cf3451293594b3cb55f3ece9b6ac32feb3`  
		Last Modified: Tue, 22 Apr 2025 18:32:02 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beefa71179466d2a62c23f183e3b7f66552c4a83ddffebe059ec84aa627ed404`  
		Last Modified: Tue, 22 Apr 2025 18:32:02 GMT  
		Size: 4.8 KB (4829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:9bca963b9346eaa91c054d7dc9676e64770c6c1dbd8fcbdf8b202f05caa662aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b9055acddda5525a8089bfda90b61a490b7085396e2ff288a1bf74d1c93a6c`

```dockerfile
```

-	Layers:
	-	`sha256:ebaad4ee017c9a6f55fa5d518d90f0afc2b5d88ecc78d43d423781844ac3f976`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 34.6 KB (34643 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.16`

```console
$ docker pull percona@sha256:c02e9bb4bc78fc69b2ec21de36dfabe4de2002ae654a7ed200cfb08447c0449e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.16` - linux; amd64

```console
$ docker pull percona@sha256:50e298cd551cd71ff803b7393910758ed030bbb42856886c09fb20288144b217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260309885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e06d1950eb8d3d87c5ff69bc83f2df11affd95e9ec39e4b98945269299b0aa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e296324865139a0256e5b0c24c56b13abc0ffbc4187b84d97c16faf4a2ed42`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 8.0 MB (7955244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feff4dd39d2418ebf2c2ee3d6e144890c6bef994dd25990c33cd67d749e376a8`  
		Last Modified: Tue, 22 Apr 2025 18:32:07 GMT  
		Size: 212.0 MB (211995330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492e4641fcd852c3509863d434da0ecc7b3df29bab240071e5b71afa6b43cba`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f1e8594ca8bb14b1131d84ce370d42084e8f4e7cb7099c8a5ab80b30916f2`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f5565eba0829883af857c4e1bfd626499509f78cba7cd51ac373f05928a5fa`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e2b86f95f4cf558bf317db4e1e6523fb38b4cfcd32001906aa46ef56e5a56`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c3b61046ef9fa0a0e2f7187f3a15fefecff5507784d6753ebc3e8323e0a27a`  
		Last Modified: Tue, 22 Apr 2025 18:32:01 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a85065b015a733f051a6bb00417cf3451293594b3cb55f3ece9b6ac32feb3`  
		Last Modified: Tue, 22 Apr 2025 18:32:02 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beefa71179466d2a62c23f183e3b7f66552c4a83ddffebe059ec84aa627ed404`  
		Last Modified: Tue, 22 Apr 2025 18:32:02 GMT  
		Size: 4.8 KB (4829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.16` - unknown; unknown

```console
$ docker pull percona@sha256:9bca963b9346eaa91c054d7dc9676e64770c6c1dbd8fcbdf8b202f05caa662aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b9055acddda5525a8089bfda90b61a490b7085396e2ff288a1bf74d1c93a6c`

```dockerfile
```

-	Layers:
	-	`sha256:ebaad4ee017c9a6f55fa5d518d90f0afc2b5d88ecc78d43d423781844ac3f976`  
		Last Modified: Tue, 22 Apr 2025 18:32:00 GMT  
		Size: 34.6 KB (34643 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:f230e5642f2eef11a9b55db89f90a06e8eac4adcf2ded82128b3a8a82f270dfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:5caf942c6e523bb0477a249916bfe04a9a461d145c25e1698d684551fd0a2731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276951001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ebec14447ccf2e2c17c074ed49b2f7bf288617a04c6b43356dba5b8e0fa0ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b3f3daa017c23ddc1e8a8dd05ca791e3ff3a4aee0b11c4012b9a0f2b306d75`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 8.0 MB (7955218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dcd6e5c9b070a46290c92f36846d13eee937f5c20af6eafa721f28458dee68`  
		Last Modified: Tue, 22 Apr 2025 18:32:13 GMT  
		Size: 228.6 MB (228636472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b9d0d51ecc0f0fddd84c17552dbf96a26d629662532e0e6ad91d09a103fc`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7d025de0b9464743ff419150202fe301401f54a192d4cb9ccdecfc30ff951`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff999e5ef9fa81579857a98cf58177086a2b9e60dea8ef9fae2693c8ec8e4b`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d354fcbfa5859741464d8a47e4bf42ee9f3cfb0669e7e2252d30ccd3924ed75e`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451bf62981b90d3dd6244015fd9b833926200499b291a2d33cef6d6fd6ffe147`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28e55e459f4f2ecd25a133ad151020953c9df8e8a5d83b335b15c2de575593`  
		Last Modified: Tue, 22 Apr 2025 18:32:11 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b860cef233590c262938feeea8c76010f3771fc0e66f5264b3e16eeaed33fe`  
		Last Modified: Tue, 22 Apr 2025 18:32:11 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:3445f22866d57c449583e72422bd139932af517159aa4f85d548b9795477f55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e06037696258c9fcea22dc32cdc193917cb05ee74ad14469d4a4f15d83ce289`

```dockerfile
```

-	Layers:
	-	`sha256:2846c0b8c455b02b8bae7800c69007be413f0e35452cdee13c87e727c37ad168`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.4`

```console
$ docker pull percona@sha256:f230e5642f2eef11a9b55db89f90a06e8eac4adcf2ded82128b3a8a82f270dfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.4` - linux; amd64

```console
$ docker pull percona@sha256:5caf942c6e523bb0477a249916bfe04a9a461d145c25e1698d684551fd0a2731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276951001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ebec14447ccf2e2c17c074ed49b2f7bf288617a04c6b43356dba5b8e0fa0ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b3f3daa017c23ddc1e8a8dd05ca791e3ff3a4aee0b11c4012b9a0f2b306d75`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 8.0 MB (7955218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dcd6e5c9b070a46290c92f36846d13eee937f5c20af6eafa721f28458dee68`  
		Last Modified: Tue, 22 Apr 2025 18:32:13 GMT  
		Size: 228.6 MB (228636472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b9d0d51ecc0f0fddd84c17552dbf96a26d629662532e0e6ad91d09a103fc`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7d025de0b9464743ff419150202fe301401f54a192d4cb9ccdecfc30ff951`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff999e5ef9fa81579857a98cf58177086a2b9e60dea8ef9fae2693c8ec8e4b`  
		Last Modified: Tue, 22 Apr 2025 18:32:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d354fcbfa5859741464d8a47e4bf42ee9f3cfb0669e7e2252d30ccd3924ed75e`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451bf62981b90d3dd6244015fd9b833926200499b291a2d33cef6d6fd6ffe147`  
		Last Modified: Tue, 22 Apr 2025 18:32:10 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28e55e459f4f2ecd25a133ad151020953c9df8e8a5d83b335b15c2de575593`  
		Last Modified: Tue, 22 Apr 2025 18:32:11 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b860cef233590c262938feeea8c76010f3771fc0e66f5264b3e16eeaed33fe`  
		Last Modified: Tue, 22 Apr 2025 18:32:11 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.4` - unknown; unknown

```console
$ docker pull percona@sha256:3445f22866d57c449583e72422bd139932af517159aa4f85d548b9795477f55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e06037696258c9fcea22dc32cdc193917cb05ee74ad14469d4a4f15d83ce289`

```dockerfile
```

-	Layers:
	-	`sha256:2846c0b8c455b02b8bae7800c69007be413f0e35452cdee13c87e727c37ad168`  
		Last Modified: Tue, 22 Apr 2025 18:32:08 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json
