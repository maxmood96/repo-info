<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.44-35`](#percona8044-35)
-	[`percona:8.0.44-35-centos`](#percona8044-35-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.44-35`](#perconaps-8044-35)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.27`](#perconapsmdb-6027)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.28`](#perconapsmdb-7028)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.17`](#perconapsmdb-8017)

## `percona:8`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.44-35`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.44-35` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.44-35` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.44-35-centos`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.44-35-centos` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.44-35-centos` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.44-35`

```console
$ docker pull percona@sha256:bfdd8dfe8193b468add8a4ed8a8480f11c640177625ee865d7174827c85e824f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.44-35` - linux; amd64

```console
$ docker pull percona@sha256:85d152758a26c4e4851dc7909e61c2181b0c2ae67b92aab1c0ebd12c0ae38830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428018634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200dc5129f2e08f3238a83b7951ab35303364cd0696c49919422028e547439a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:35 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:35 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_VERSION=8.0.44-35.1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_PERCONA_VERSION=8.0.44-35.1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.44-1.el9
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_REPO=testing
# Thu, 04 Dec 2025 19:46:35 GMT
ENV PS_TELEMETRY_VERSION=8.0.44-35-1
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:35 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 04 Dec 2025 19:46:35 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:35 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 04 Dec 2025 19:47:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:47:11 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:11 GMT
USER mysql
# Thu, 04 Dec 2025 19:47:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 04 Dec 2025 19:47:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc679cf4c4466559170a395e22b06a82d3a268e715398190e2740d93045ede`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870faf7464e7960ce6e5ed6b759e6906f96d3d1c82d89afcc90936d4f560fe9`  
		Last Modified: Thu, 04 Dec 2025 19:48:09 GMT  
		Size: 9.2 MB (9187049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b858abf119453e03b12207ecb10434e0f4b6a976e846891c0e2fbc8017a8e`  
		Last Modified: Thu, 04 Dec 2025 19:48:02 GMT  
		Size: 378.8 MB (378781091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fa6a169d31d16f74e1b4fa508bea9d1a8dbf2b3791438c9ba329d036c1176`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1f8699fe9d08895ae3724540f41bd62ff19cdb3d18df6c4ad67a9444e8f8c`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d5ee01dcc962ad4249cc25fbf391890977d98ecc9c8c903551bf725736718`  
		Last Modified: Thu, 04 Dec 2025 19:48:08 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.44-35` - unknown; unknown

```console
$ docker pull percona@sha256:175fc90c7e0d0ca5a3a718c4bf0aad6b7dc3f4714a670c6d27d5db7b801da1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab5f3aeabac989ce9e9ea9b333262bd666c52fdd7513023841b9843bebf58f`

```dockerfile
```

-	Layers:
	-	`sha256:0ffed152d3b21902c0bf414356182fd1485401c48b298d230889821eb9d59445`  
		Last Modified: Thu, 04 Dec 2025 21:10:58 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:7ab654ba1fc707ae7a6f0890752c133a86d494139864af9d453ca5c21364ef95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:849572e83ff90609fd789ad8bc82ab5461e8b426d2013171b0d65dc87fd2abf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272192193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a455cad0d39e5f7da25c4259c173deeace37b8689a594622f09bdb88e72ab97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Mon, 12 Jan 2026 20:02:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 12 Jan 2026 20:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 12 Jan 2026 20:02:08 GMT
ENV PSMDB_VERSION=6.0.27-21
# Mon, 12 Jan 2026 20:02:08 GMT
ENV OS_VER=el9
# Mon, 12 Jan 2026 20:02:08 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Mon, 12 Jan 2026 20:02:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 12 Jan 2026 20:02:08 GMT
ENV PSMDB_REPO=release
# Mon, 12 Jan 2026 20:02:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 12 Jan 2026 20:02:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 12 Jan 2026 20:02:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
ENV GOSU_VERSION=1.11
# Mon, 12 Jan 2026 20:02:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 12 Jan 2026 20:02:24 GMT
VOLUME [/data/db]
# Mon, 12 Jan 2026 20:02:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 12 Jan 2026 20:02:25 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 20:02:25 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 12 Jan 2026 20:02:25 GMT
USER 1001
# Mon, 12 Jan 2026 20:02:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8bd755cb676630a4b12103abd268ee9b6dc00489acd0026b816b774aa13011`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 8.9 MB (8864054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61d9e076267ac93d540e927566212bda5a72dfb31d8f4afa151159a1ac3cdc5`  
		Last Modified: Mon, 12 Jan 2026 20:04:50 GMT  
		Size: 222.3 MB (222334534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991357a2acf4c04875e7c1cd713eb9e1b0137c922c8706dec73ce4fd701d928f`  
		Last Modified: Mon, 12 Jan 2026 20:03:19 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79a3f942548357deb97c12b3c393ad516b1b6e6cf13fc2e2602697011c697ae`  
		Last Modified: Mon, 12 Jan 2026 20:02:51 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c3be34c2be40cb625f65bf1af24b9963971b831d9ef7f39bea295380388367`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae14061483fdf2a067bbd55ddde9156613998f244a9e3f06804febdba71d673`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fa4b9b4049d3c01f7439b330451242e842a2818c7c25dcef09fd7ff57c9a2`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6827e3d0d004dd26e13384a2465dbb5381501af067e6f5af5d2dd0810d1817ba`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e075153146dcef15093c191c67031cb8bcc28da83444be5843c3c3f7fb96ee`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:f1a810d27e4b26c1ef664da0106089fd169f51edbd3cccab98e004940c950aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d5f8cb27c2f5daf4f03d52fb63af241b5777b0a8da1b92fbb8ceeabb6a93e5`

```dockerfile
```

-	Layers:
	-	`sha256:8e8eddd98a40c1e1b3f032191ce6f004ba3f9ed872837f7fe8788ee9939a2b7f`  
		Last Modified: Mon, 12 Jan 2026 20:02:51 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.27`

```console
$ docker pull percona@sha256:7ab654ba1fc707ae7a6f0890752c133a86d494139864af9d453ca5c21364ef95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.27` - linux; amd64

```console
$ docker pull percona@sha256:849572e83ff90609fd789ad8bc82ab5461e8b426d2013171b0d65dc87fd2abf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272192193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a455cad0d39e5f7da25c4259c173deeace37b8689a594622f09bdb88e72ab97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Mon, 12 Jan 2026 20:02:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 12 Jan 2026 20:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 12 Jan 2026 20:02:08 GMT
ENV PSMDB_VERSION=6.0.27-21
# Mon, 12 Jan 2026 20:02:08 GMT
ENV OS_VER=el9
# Mon, 12 Jan 2026 20:02:08 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Mon, 12 Jan 2026 20:02:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 12 Jan 2026 20:02:08 GMT
ENV PSMDB_REPO=release
# Mon, 12 Jan 2026 20:02:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 12 Jan 2026 20:02:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 12 Jan 2026 20:02:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 12 Jan 2026 20:02:22 GMT
ENV GOSU_VERSION=1.11
# Mon, 12 Jan 2026 20:02:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 12 Jan 2026 20:02:24 GMT
VOLUME [/data/db]
# Mon, 12 Jan 2026 20:02:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 12 Jan 2026 20:02:25 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 20:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 20:02:25 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 12 Jan 2026 20:02:25 GMT
USER 1001
# Mon, 12 Jan 2026 20:02:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8bd755cb676630a4b12103abd268ee9b6dc00489acd0026b816b774aa13011`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 8.9 MB (8864054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61d9e076267ac93d540e927566212bda5a72dfb31d8f4afa151159a1ac3cdc5`  
		Last Modified: Mon, 12 Jan 2026 20:04:50 GMT  
		Size: 222.3 MB (222334534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991357a2acf4c04875e7c1cd713eb9e1b0137c922c8706dec73ce4fd701d928f`  
		Last Modified: Mon, 12 Jan 2026 20:03:19 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79a3f942548357deb97c12b3c393ad516b1b6e6cf13fc2e2602697011c697ae`  
		Last Modified: Mon, 12 Jan 2026 20:02:51 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c3be34c2be40cb625f65bf1af24b9963971b831d9ef7f39bea295380388367`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae14061483fdf2a067bbd55ddde9156613998f244a9e3f06804febdba71d673`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fa4b9b4049d3c01f7439b330451242e842a2818c7c25dcef09fd7ff57c9a2`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6827e3d0d004dd26e13384a2465dbb5381501af067e6f5af5d2dd0810d1817ba`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e075153146dcef15093c191c67031cb8bcc28da83444be5843c3c3f7fb96ee`  
		Last Modified: Mon, 12 Jan 2026 20:03:12 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.27` - unknown; unknown

```console
$ docker pull percona@sha256:f1a810d27e4b26c1ef664da0106089fd169f51edbd3cccab98e004940c950aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d5f8cb27c2f5daf4f03d52fb63af241b5777b0a8da1b92fbb8ceeabb6a93e5`

```dockerfile
```

-	Layers:
	-	`sha256:8e8eddd98a40c1e1b3f032191ce6f004ba3f9ed872837f7fe8788ee9939a2b7f`  
		Last Modified: Mon, 12 Jan 2026 20:02:51 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:2c9bda7cf3fc9a3a7d210b5a98b0fee607c266e38385401ee5c033955dff2f12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:d1fbf00e7abc1fb8749a03a1c7de0e8f51aeeefd4a2a019442a0dfc44c85de02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288026797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9acba0e205080947b659f80291c1db94edd615f58c04816b5c989b460cefd35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 08 Jan 2026 19:04:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 08 Jan 2026 19:04:16 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 08 Jan 2026 19:04:16 GMT
ENV PSMDB_VERSION=7.0.28-15
# Thu, 08 Jan 2026 19:04:16 GMT
ENV OS_VER=el9
# Thu, 08 Jan 2026 19:04:16 GMT
ENV FULL_PERCONA_VERSION=7.0.28-15.el9
# Thu, 08 Jan 2026 19:04:16 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 08 Jan 2026 19:04:16 GMT
ENV PSMDB_REPO=release
# Thu, 08 Jan 2026 19:04:16 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 08 Jan 2026 19:04:16 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 08 Jan 2026 19:04:16 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 08 Jan 2026 19:04:32 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 08 Jan 2026 19:04:32 GMT
VOLUME [/data/db]
# Thu, 08 Jan 2026 19:04:33 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 08 Jan 2026 19:04:33 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:33 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 08 Jan 2026 19:04:33 GMT
USER 1001
# Thu, 08 Jan 2026 19:04:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbcaf045f2b27a75de471b1a539846bfd1d5a34535086af739779b135fe2d72`  
		Last Modified: Thu, 08 Jan 2026 19:06:03 GMT  
		Size: 8.9 MB (8855532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d9e7ddc4925f06fdfe91409895f5b1c9a3ddd9a08fac4391024f8504179c9`  
		Last Modified: Thu, 08 Jan 2026 19:06:09 GMT  
		Size: 238.2 MB (238177663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcb81132f3e4c44994586fdce9ad815bcf908cb0cd1c54f403a5380b4fa8e3f`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5b6c7f1057a3167fa18d7e45b1fdfc3f8b833ec6e45d020212414a9a4a5ee`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fab0fdd71a04646e37e7669f26af527d99226299e7c2716ec4f92a01c3636e`  
		Last Modified: Thu, 08 Jan 2026 19:05:01 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ffddb04e02c904f115c57c38c5be2c1be2f14db5c9f95ebde5183e8c41e0f3`  
		Last Modified: Thu, 08 Jan 2026 19:05:01 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d95f1adda25f202afc0c1b94bf0c8eabb58d89f640089a4d50090775149429f`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920369ebf4924fff8a7634ffac41acdb8eec9c8fcfb7fd92b5dee446daea2c0f`  
		Last Modified: Thu, 08 Jan 2026 19:06:03 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e6bea390392d8f2b8d014ab05a052723c3664271dcf586c94c29cfdb4a6b0`  
		Last Modified: Thu, 08 Jan 2026 19:05:02 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:69431c42c3fa54766459f36eb7391c845ec3b6f23f3e9a7da7b593294358873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc6b5c1ef70f4921963ddb6ee2e27d138fc0da72ab76c721fc0166e293f51c4`

```dockerfile
```

-	Layers:
	-	`sha256:0affa3200abfdaa58acbbb3234e9417c415d71e4280d27761f82ae324ae2a4df`  
		Last Modified: Thu, 08 Jan 2026 21:10:22 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.28`

```console
$ docker pull percona@sha256:2c9bda7cf3fc9a3a7d210b5a98b0fee607c266e38385401ee5c033955dff2f12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.28` - linux; amd64

```console
$ docker pull percona@sha256:d1fbf00e7abc1fb8749a03a1c7de0e8f51aeeefd4a2a019442a0dfc44c85de02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288026797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9acba0e205080947b659f80291c1db94edd615f58c04816b5c989b460cefd35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 08 Jan 2026 19:04:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 08 Jan 2026 19:04:16 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 08 Jan 2026 19:04:16 GMT
ENV PSMDB_VERSION=7.0.28-15
# Thu, 08 Jan 2026 19:04:16 GMT
ENV OS_VER=el9
# Thu, 08 Jan 2026 19:04:16 GMT
ENV FULL_PERCONA_VERSION=7.0.28-15.el9
# Thu, 08 Jan 2026 19:04:16 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 08 Jan 2026 19:04:16 GMT
ENV PSMDB_REPO=release
# Thu, 08 Jan 2026 19:04:16 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 08 Jan 2026 19:04:16 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 08 Jan 2026 19:04:16 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 08 Jan 2026 19:04:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 08 Jan 2026 19:04:32 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 08 Jan 2026 19:04:32 GMT
VOLUME [/data/db]
# Thu, 08 Jan 2026 19:04:33 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 08 Jan 2026 19:04:33 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:04:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:33 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 08 Jan 2026 19:04:33 GMT
USER 1001
# Thu, 08 Jan 2026 19:04:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbcaf045f2b27a75de471b1a539846bfd1d5a34535086af739779b135fe2d72`  
		Last Modified: Thu, 08 Jan 2026 19:06:03 GMT  
		Size: 8.9 MB (8855532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d9e7ddc4925f06fdfe91409895f5b1c9a3ddd9a08fac4391024f8504179c9`  
		Last Modified: Thu, 08 Jan 2026 19:06:09 GMT  
		Size: 238.2 MB (238177663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcb81132f3e4c44994586fdce9ad815bcf908cb0cd1c54f403a5380b4fa8e3f`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5b6c7f1057a3167fa18d7e45b1fdfc3f8b833ec6e45d020212414a9a4a5ee`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fab0fdd71a04646e37e7669f26af527d99226299e7c2716ec4f92a01c3636e`  
		Last Modified: Thu, 08 Jan 2026 19:05:01 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ffddb04e02c904f115c57c38c5be2c1be2f14db5c9f95ebde5183e8c41e0f3`  
		Last Modified: Thu, 08 Jan 2026 19:05:01 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d95f1adda25f202afc0c1b94bf0c8eabb58d89f640089a4d50090775149429f`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920369ebf4924fff8a7634ffac41acdb8eec9c8fcfb7fd92b5dee446daea2c0f`  
		Last Modified: Thu, 08 Jan 2026 19:06:03 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e6bea390392d8f2b8d014ab05a052723c3664271dcf586c94c29cfdb4a6b0`  
		Last Modified: Thu, 08 Jan 2026 19:05:02 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.28` - unknown; unknown

```console
$ docker pull percona@sha256:69431c42c3fa54766459f36eb7391c845ec3b6f23f3e9a7da7b593294358873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc6b5c1ef70f4921963ddb6ee2e27d138fc0da72ab76c721fc0166e293f51c4`

```dockerfile
```

-	Layers:
	-	`sha256:0affa3200abfdaa58acbbb3234e9417c415d71e4280d27761f82ae324ae2a4df`  
		Last Modified: Thu, 08 Jan 2026 21:10:22 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:21e6eafc0664e7ff65e5ef9eaace4120f0f74ac1b5164b9034e32588e6afcfb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:999597fc997cb83d92bffdeb37fafcbf07b9973183e8a5dc7efb87176b95ac21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307639091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcdef03a344105eee1f6df8f9a12942bd01e1cc879313e0230cbd41295ec57b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 08 Jan 2026 19:04:21 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 08 Jan 2026 19:04:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 08 Jan 2026 19:04:21 GMT
ENV PSMDB_VERSION=8.0.17-6
# Thu, 08 Jan 2026 19:04:21 GMT
ENV OS_VER=el9
# Thu, 08 Jan 2026 19:04:21 GMT
ENV FULL_PERCONA_VERSION=8.0.17-6.el9
# Thu, 08 Jan 2026 19:04:21 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 08 Jan 2026 19:04:21 GMT
ENV PSMDB_REPO=testing
# Thu, 08 Jan 2026 19:04:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 08 Jan 2026 19:04:21 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 08 Jan 2026 19:04:21 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 08 Jan 2026 19:04:21 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 08 Jan 2026 19:04:35 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 08 Jan 2026 19:04:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 08 Jan 2026 19:04:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
VOLUME [/data/db]
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 08 Jan 2026 19:04:38 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:38 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 08 Jan 2026 19:04:38 GMT
USER 1001
# Thu, 08 Jan 2026 19:04:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233f8b82555e5600ad4a1b8505ac5a3eac397ecc3245f320c4584d7529929c4`  
		Last Modified: Thu, 08 Jan 2026 19:05:06 GMT  
		Size: 8.9 MB (8855533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec55e15ffba0085cf7a57e1529590bad5fb25b8051fcc211e49c71d52d80c2c5`  
		Last Modified: Thu, 08 Jan 2026 19:05:52 GMT  
		Size: 257.8 MB (257789970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b331c37e5c44724983b6742e2169d8e54b2c7e5a8a5969dfeed01b539eaf633b`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3aa49b180fa547cbac7f1a3fd258a265586f6345c9bc3ae69e168540a6602`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6968dadd4c7d0b18a9c8199aca1daf244ff7ce0a4f0cd32e58cf27e4029db89`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f316bb041fbb8b1131d378b16bcc38144bc7797e0c15842520f73f5c81b012c`  
		Last Modified: Thu, 08 Jan 2026 19:05:50 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f38251cf9c8e608869a672adb120466f5c2ec2af6438477448e325544391440`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534255af5a9fc84e7d5fca5071eae4d4274442525f0876ffac040c8c45b19e8d`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957347392b38ad3a3470123578b529e46ece129b7a9c33128f1d0b40ceccb6a8`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:fc823fd6a74b6b1a809ed6651aaa55c7f5ba80809525900b168231fd6d9752a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e674e137c240b3494953ef26023f58871e6a6d31cd7f49bf71cd4b9e17179`

```dockerfile
```

-	Layers:
	-	`sha256:0fb77e2cdb428a51f5d95a333e65bd7f833505cf758fdd513c4766cdae41111b`  
		Last Modified: Thu, 08 Jan 2026 21:10:30 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.17`

```console
$ docker pull percona@sha256:21e6eafc0664e7ff65e5ef9eaace4120f0f74ac1b5164b9034e32588e6afcfb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.17` - linux; amd64

```console
$ docker pull percona@sha256:999597fc997cb83d92bffdeb37fafcbf07b9973183e8a5dc7efb87176b95ac21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307639091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcdef03a344105eee1f6df8f9a12942bd01e1cc879313e0230cbd41295ec57b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 08 Jan 2026 19:04:21 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 08 Jan 2026 19:04:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 08 Jan 2026 19:04:21 GMT
ENV PSMDB_VERSION=8.0.17-6
# Thu, 08 Jan 2026 19:04:21 GMT
ENV OS_VER=el9
# Thu, 08 Jan 2026 19:04:21 GMT
ENV FULL_PERCONA_VERSION=8.0.17-6.el9
# Thu, 08 Jan 2026 19:04:21 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 08 Jan 2026 19:04:21 GMT
ENV PSMDB_REPO=testing
# Thu, 08 Jan 2026 19:04:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 08 Jan 2026 19:04:21 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 08 Jan 2026 19:04:21 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 08 Jan 2026 19:04:21 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 08 Jan 2026 19:04:35 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 08 Jan 2026 19:04:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 08 Jan 2026 19:04:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
VOLUME [/data/db]
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 08 Jan 2026 19:04:38 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:04:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:38 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 08 Jan 2026 19:04:38 GMT
USER 1001
# Thu, 08 Jan 2026 19:04:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233f8b82555e5600ad4a1b8505ac5a3eac397ecc3245f320c4584d7529929c4`  
		Last Modified: Thu, 08 Jan 2026 19:05:06 GMT  
		Size: 8.9 MB (8855533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec55e15ffba0085cf7a57e1529590bad5fb25b8051fcc211e49c71d52d80c2c5`  
		Last Modified: Thu, 08 Jan 2026 19:05:52 GMT  
		Size: 257.8 MB (257789970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b331c37e5c44724983b6742e2169d8e54b2c7e5a8a5969dfeed01b539eaf633b`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3aa49b180fa547cbac7f1a3fd258a265586f6345c9bc3ae69e168540a6602`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6968dadd4c7d0b18a9c8199aca1daf244ff7ce0a4f0cd32e58cf27e4029db89`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f316bb041fbb8b1131d378b16bcc38144bc7797e0c15842520f73f5c81b012c`  
		Last Modified: Thu, 08 Jan 2026 19:05:50 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f38251cf9c8e608869a672adb120466f5c2ec2af6438477448e325544391440`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534255af5a9fc84e7d5fca5071eae4d4274442525f0876ffac040c8c45b19e8d`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957347392b38ad3a3470123578b529e46ece129b7a9c33128f1d0b40ceccb6a8`  
		Last Modified: Thu, 08 Jan 2026 19:05:47 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.17` - unknown; unknown

```console
$ docker pull percona@sha256:fc823fd6a74b6b1a809ed6651aaa55c7f5ba80809525900b168231fd6d9752a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e674e137c240b3494953ef26023f58871e6a6d31cd7f49bf71cd4b9e17179`

```dockerfile
```

-	Layers:
	-	`sha256:0fb77e2cdb428a51f5d95a333e65bd7f833505cf758fdd513c4766cdae41111b`  
		Last Modified: Thu, 08 Jan 2026 21:10:30 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
