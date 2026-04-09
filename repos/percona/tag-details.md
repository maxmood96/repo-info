<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.45-36`](#percona8045-36)
-	[`percona:8.0.45-36-centos`](#percona8045-36-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.45-35`](#perconaps-8045-35)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.27`](#perconapsmdb-6027)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.31`](#perconapsmdb-7031)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.20`](#perconapsmdb-8020)

## `percona:8`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.45-36`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.45-36` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.45-36` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.45-36-centos`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.45-36-centos` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.45-36-centos` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.45-35`

```console
$ docker pull percona@sha256:2596ee4ed1db6dd814d157f12aebd75985e85bfc6ef5b34aed663348e4181113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.45-35` - linux; amd64

```console
$ docker pull percona@sha256:04608b40e050a3e3e677014c084747e5b90dc2ebc3076ed33a2c773a3151d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428609567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893ea3a1a14abd1a8c616df5387f7a3094d56381ec0a110445e636353b7d9c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:42 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_VERSION=8.0.45-36.1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_REPO=testing
# Wed, 08 Apr 2026 17:23:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:42 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Apr 2026 17:23:42 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:23:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
USER mysql
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca86541411699def937f124805d6add55755151dc6a0317d949abc8c167f08`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5165cee991db64c4cb794ff99f7cf76515b6a73b3c4b5dd0b6b927a702da27b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 9.2 MB (9222700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631c99da4b0d0ee727ed2634ea46fe9fdcac2bd287f0a8d0b1f8c1fb0293d23`  
		Last Modified: Wed, 08 Apr 2026 17:25:12 GMT  
		Size: 379.4 MB (379394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042588cc13ad5cfeb1e03e9ca840d6d2e4e0ea81de053ce974a6bc896f8478b`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f35995037a69e8f72b52d8755377ef0b0f0a6f99311594416784001089f25`  
		Last Modified: Wed, 08 Apr 2026 17:25:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.45-35` - unknown; unknown

```console
$ docker pull percona@sha256:82b86ea2595502f685b836e3dce5c4090c431e30686ec569cebe5124c1746190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed9c6de5ceb6a860414abc7fd118e2c38b5940bce3e626635877d9b1dce430`

```dockerfile
```

-	Layers:
	-	`sha256:dbfe30db876820b23513aa9d190b1eab7d9890129832ca69a0b7771cdc72524c`  
		Last Modified: Wed, 08 Apr 2026 17:25:05 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:2eb7837de0439fe40acdef0826e4bb2946964a0a9bb62b3c6632d466ad944870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:8962ca02bcb09906da7a43e1545d60c80cfd9aea20702bdb6ef23fd71272baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269283399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb8d3f82c4e0793b0bac9a8a7aac1c2bc36c9e3a080c0e442be965cba5496be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:24:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:24:57 GMT
ENV PSMDB_VERSION=6.0.27-21
# Wed, 08 Apr 2026 17:24:57 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:24:57 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Wed, 08 Apr 2026 17:24:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:24:57 GMT
ENV PSMDB_REPO=release
# Wed, 08 Apr 2026 17:24:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:24:57 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:24:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:25:12 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:25:12 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:25:12 GMT
USER 1001
# Wed, 08 Apr 2026 17:25:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd93d434a835695b72308e471ac2e60725b16b0bcdf2e4447cac16d2edb9068d`  
		Last Modified: Wed, 08 Apr 2026 17:25:47 GMT  
		Size: 8.8 MB (8847866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b941e5fcccd7838962b624494a32ab83687a20e7d7cfe6541c665a2e67e58c08`  
		Last Modified: Wed, 08 Apr 2026 17:25:51 GMT  
		Size: 219.5 MB (219500046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a37e6e1b19f464635489a5edd315a68c5fb26ba463d1b675d37d0107c8b2f39`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4c488b8b37b95e9a5de88315aed0d4c8b878f5e2697ebcd92047d4d782e280`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26377115308e6b6005bc5a058e4c1df3465be71d48dd692b6af677eb0823553`  
		Last Modified: Wed, 08 Apr 2026 17:25:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e552250a547e27d70f8f938f17ba47db95dc5539529753c2eeaf60259745c6`  
		Last Modified: Wed, 08 Apr 2026 17:25:48 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b480d0dbed2fd6012fb1c5cacca38149cb9b0b10d9056afb7d27153d491a8`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3d0e842682b0ca84dda14a3e34b25d46e2357a168df115c089c9cf0e6b59c3`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ecc705392e50aab4cca086548f1eee142e11d9965cdc7dd1f6d249ca0d90af`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:209640e30b26629bd2ab4add971183f9e4f0f2bfebe1798bd22a92de6293f93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46981dabba7dfb16be907464e7e13f07182a79960ad158debaee88bbc01f2f2e`

```dockerfile
```

-	Layers:
	-	`sha256:6ebff7f37d298b0e4beff8c3f2dfffa51099b7e03aa706fd534cce7fbe2a132b`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.27`

```console
$ docker pull percona@sha256:2eb7837de0439fe40acdef0826e4bb2946964a0a9bb62b3c6632d466ad944870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.27` - linux; amd64

```console
$ docker pull percona@sha256:8962ca02bcb09906da7a43e1545d60c80cfd9aea20702bdb6ef23fd71272baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269283399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb8d3f82c4e0793b0bac9a8a7aac1c2bc36c9e3a080c0e442be965cba5496be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:24:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:24:57 GMT
ENV PSMDB_VERSION=6.0.27-21
# Wed, 08 Apr 2026 17:24:57 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:24:57 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Wed, 08 Apr 2026 17:24:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:24:57 GMT
ENV PSMDB_REPO=release
# Wed, 08 Apr 2026 17:24:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:24:57 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:24:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:25:10 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:25:12 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:25:12 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:25:12 GMT
USER 1001
# Wed, 08 Apr 2026 17:25:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd93d434a835695b72308e471ac2e60725b16b0bcdf2e4447cac16d2edb9068d`  
		Last Modified: Wed, 08 Apr 2026 17:25:47 GMT  
		Size: 8.8 MB (8847866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b941e5fcccd7838962b624494a32ab83687a20e7d7cfe6541c665a2e67e58c08`  
		Last Modified: Wed, 08 Apr 2026 17:25:51 GMT  
		Size: 219.5 MB (219500046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a37e6e1b19f464635489a5edd315a68c5fb26ba463d1b675d37d0107c8b2f39`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4c488b8b37b95e9a5de88315aed0d4c8b878f5e2697ebcd92047d4d782e280`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26377115308e6b6005bc5a058e4c1df3465be71d48dd692b6af677eb0823553`  
		Last Modified: Wed, 08 Apr 2026 17:25:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e552250a547e27d70f8f938f17ba47db95dc5539529753c2eeaf60259745c6`  
		Last Modified: Wed, 08 Apr 2026 17:25:48 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b480d0dbed2fd6012fb1c5cacca38149cb9b0b10d9056afb7d27153d491a8`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3d0e842682b0ca84dda14a3e34b25d46e2357a168df115c089c9cf0e6b59c3`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ecc705392e50aab4cca086548f1eee142e11d9965cdc7dd1f6d249ca0d90af`  
		Last Modified: Wed, 08 Apr 2026 17:25:49 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.27` - unknown; unknown

```console
$ docker pull percona@sha256:209640e30b26629bd2ab4add971183f9e4f0f2bfebe1798bd22a92de6293f93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46981dabba7dfb16be907464e7e13f07182a79960ad158debaee88bbc01f2f2e`

```dockerfile
```

-	Layers:
	-	`sha256:6ebff7f37d298b0e4beff8c3f2dfffa51099b7e03aa706fd534cce7fbe2a132b`  
		Last Modified: Wed, 08 Apr 2026 17:25:46 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:aa41970809f8c087165d8598c963cd968f7ba583bf2f29bee04ce0e4e18f4cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:f1f637258f8d4a34736b2fe17579012bb1b957bcb5cecd336df0db0cc0274c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300194407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338fc2ad38a6c4821d4e73d8a53aa41465b3136dec3b2ae86005e27c2ab0bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_VERSION=7.0.31-17
# Wed, 08 Apr 2026 17:23:47 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV FULL_PERCONA_VERSION=7.0.31-17.el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_REPO=release
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:05 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:06 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:06 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:06 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fec4e3ba2497a613252e5571c10184b78ed722483394645ff8496a6a4f31bb`  
		Last Modified: Wed, 08 Apr 2026 17:24:39 GMT  
		Size: 8.8 MB (8843977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f53357bc4513beabd7fc1daa6d39b8d33b58b41bf8d935593ab6d087aa69943`  
		Last Modified: Wed, 08 Apr 2026 17:24:46 GMT  
		Size: 250.4 MB (250414940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1f7f3f93308aea592261b1eddf51b60015f249bb4902c995d31cd253b57a99`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e239411b0396d8349a200d04981f6bb1f399b10e2ca9a103b731d7ed65fe1d7`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50934fdf3d8ba4ec99e94a3004c884294b7245bbb4b9153e89ecc4239595e39c`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19ab7095c2e99c649dc9a1aedae3917a765820cb642730cec7acb8cd9922cc8`  
		Last Modified: Wed, 08 Apr 2026 17:24:41 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e39a207e1276d25100ff80e389c7360b7939934251440a9ddf34e624f63c5`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec12a334e14c251048ba879275912758a2a8ecf9003bd3eeb3a83c5abb158c0`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6896e3d913f19efbf3c340825f36e8569cad483eb0d8815ba486ef41b582731f`  
		Last Modified: Wed, 08 Apr 2026 17:24:43 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:3bfbd1b773b09cf64321d55455d5ac3dcdd685d2f3129ad4e01498af6eb26cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a0b553964715afb729bb17430aae9ad42fc76be7de8ea3a97ad77a7dd4864`

```dockerfile
```

-	Layers:
	-	`sha256:e8515fd9c403fff02ff879e0b4ab092b17224095c46d20532fd6e2b04dc2f09a`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.31`

```console
$ docker pull percona@sha256:aa41970809f8c087165d8598c963cd968f7ba583bf2f29bee04ce0e4e18f4cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.31` - linux; amd64

```console
$ docker pull percona@sha256:f1f637258f8d4a34736b2fe17579012bb1b957bcb5cecd336df0db0cc0274c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300194407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338fc2ad38a6c4821d4e73d8a53aa41465b3136dec3b2ae86005e27c2ab0bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_VERSION=7.0.31-17
# Wed, 08 Apr 2026 17:23:47 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV FULL_PERCONA_VERSION=7.0.31-17.el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_REPO=release
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:05 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:06 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:06 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:06 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fec4e3ba2497a613252e5571c10184b78ed722483394645ff8496a6a4f31bb`  
		Last Modified: Wed, 08 Apr 2026 17:24:39 GMT  
		Size: 8.8 MB (8843977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f53357bc4513beabd7fc1daa6d39b8d33b58b41bf8d935593ab6d087aa69943`  
		Last Modified: Wed, 08 Apr 2026 17:24:46 GMT  
		Size: 250.4 MB (250414940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1f7f3f93308aea592261b1eddf51b60015f249bb4902c995d31cd253b57a99`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e239411b0396d8349a200d04981f6bb1f399b10e2ca9a103b731d7ed65fe1d7`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50934fdf3d8ba4ec99e94a3004c884294b7245bbb4b9153e89ecc4239595e39c`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19ab7095c2e99c649dc9a1aedae3917a765820cb642730cec7acb8cd9922cc8`  
		Last Modified: Wed, 08 Apr 2026 17:24:41 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e39a207e1276d25100ff80e389c7360b7939934251440a9ddf34e624f63c5`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec12a334e14c251048ba879275912758a2a8ecf9003bd3eeb3a83c5abb158c0`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6896e3d913f19efbf3c340825f36e8569cad483eb0d8815ba486ef41b582731f`  
		Last Modified: Wed, 08 Apr 2026 17:24:43 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.31` - unknown; unknown

```console
$ docker pull percona@sha256:3bfbd1b773b09cf64321d55455d5ac3dcdd685d2f3129ad4e01498af6eb26cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a0b553964715afb729bb17430aae9ad42fc76be7de8ea3a97ad77a7dd4864`

```dockerfile
```

-	Layers:
	-	`sha256:e8515fd9c403fff02ff879e0b4ab092b17224095c46d20532fd6e2b04dc2f09a`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:6d1e73e6d6547c4e5b8c36642e468e6022382b36f869d2fcd02b4ae02f040e32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:cec963b26127c3f1b5146bd861ec5fbc91cfd6247d70c22456d817c67ae3a7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320159910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0101eb2160f7382c209ea943b6534c689f8855ad2c73e37aba139d36598224`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_VERSION=8.0.20-8
# Wed, 08 Apr 2026 17:23:56 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV FULL_PERCONA_VERSION=8.0.20-8.el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_REPO=testing
# Wed, 08 Apr 2026 17:23:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:16 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb2a02acb531c8ccab94330ecf99d49de21aeb66dc5bf4ee7a1c13b34676cb`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 8.8 MB (8844023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c726606b66c36acd816bfe14327be599d1e048f759883d3c9d96e99dbc43591`  
		Last Modified: Wed, 08 Apr 2026 17:25:00 GMT  
		Size: 270.4 MB (270380402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe96b8263b38aac6e470f3026ce6aaecabe16e7b43ce3cf88263fc120b82632c`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8828acc245febde2c1ff06a0df54b79029d0fe5df80ec71e9562bdc25e8e5`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad06daa8c97caf7be6bbd123d50139d2d31a3a5463642dc933ba47776cb5bf5`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af1f7ed81ae0ae7d02ff69bfcb25461587c0ef0e7adfd1029792cbc91d19765`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325bcd62172d458666c766cf6606b57eb83b276d912ce7330cc1570f0a17ac05`  
		Last Modified: Wed, 08 Apr 2026 17:24:56 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab225c2f86027799b49c036cb2c178ce3916eb7c34e92bd81b4f9055ee47584e`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:bfe8504b8db52d01bf9696c974af0ae53ad4674ddcb073c08f00dd057fdbc963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234dac9c14aa0be7056143994ef9d9ecf52df46b1364084bf6df56c3ac5adff`

```dockerfile
```

-	Layers:
	-	`sha256:43eb450a871f5640c475a4ccac22ff7bd4d7c7e9211fbc731458fabbbca4a287`  
		Last Modified: Wed, 08 Apr 2026 17:24:53 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.20`

```console
$ docker pull percona@sha256:6d1e73e6d6547c4e5b8c36642e468e6022382b36f869d2fcd02b4ae02f040e32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.20` - linux; amd64

```console
$ docker pull percona@sha256:cec963b26127c3f1b5146bd861ec5fbc91cfd6247d70c22456d817c67ae3a7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320159910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0101eb2160f7382c209ea943b6534c689f8855ad2c73e37aba139d36598224`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_VERSION=8.0.20-8
# Wed, 08 Apr 2026 17:23:56 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV FULL_PERCONA_VERSION=8.0.20-8.el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_REPO=testing
# Wed, 08 Apr 2026 17:23:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:16 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb2a02acb531c8ccab94330ecf99d49de21aeb66dc5bf4ee7a1c13b34676cb`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 8.8 MB (8844023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c726606b66c36acd816bfe14327be599d1e048f759883d3c9d96e99dbc43591`  
		Last Modified: Wed, 08 Apr 2026 17:25:00 GMT  
		Size: 270.4 MB (270380402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe96b8263b38aac6e470f3026ce6aaecabe16e7b43ce3cf88263fc120b82632c`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8828acc245febde2c1ff06a0df54b79029d0fe5df80ec71e9562bdc25e8e5`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad06daa8c97caf7be6bbd123d50139d2d31a3a5463642dc933ba47776cb5bf5`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af1f7ed81ae0ae7d02ff69bfcb25461587c0ef0e7adfd1029792cbc91d19765`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325bcd62172d458666c766cf6606b57eb83b276d912ce7330cc1570f0a17ac05`  
		Last Modified: Wed, 08 Apr 2026 17:24:56 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab225c2f86027799b49c036cb2c178ce3916eb7c34e92bd81b4f9055ee47584e`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.20` - unknown; unknown

```console
$ docker pull percona@sha256:bfe8504b8db52d01bf9696c974af0ae53ad4674ddcb073c08f00dd057fdbc963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234dac9c14aa0be7056143994ef9d9ecf52df46b1364084bf6df56c3ac5adff`

```dockerfile
```

-	Layers:
	-	`sha256:43eb450a871f5640c475a4ccac22ff7bd4d7c7e9211fbc731458fabbbca4a287`  
		Last Modified: Wed, 08 Apr 2026 17:24:53 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
