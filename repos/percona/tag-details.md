<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.43-34`](#percona8043-34)
-	[`percona:8.0.43-34-centos`](#percona8043-34-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.43-34`](#perconaps-8043-34)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.25`](#perconapsmdb-6025)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.24`](#perconapsmdb-7024)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.12`](#perconapsmdb-8012)

## `percona:8`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34-centos`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34-centos` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34-centos` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.43-34`

```console
$ docker pull percona@sha256:a87d569d046c92f5d2b6ec8cc550b46e5f37d530f404b90f6d55e0e526c2ebec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:dc95b1bac35bbec5bbe21cb8ede69523578e0ee3812c7cab33275e3a7ef585a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412018032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ee95085b777b33f699555ca9f5ce77c94e385afff0e5e8e4379813effeaf2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_VERSION=8.0.43-34.1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_REPO=testing
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:03 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 12 Nov 2025 00:27:03 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:03 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 12 Nov 2025 00:27:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Nov 2025 00:27:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:37 GMT
USER mysql
# Wed, 12 Nov 2025 00:27:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 12 Nov 2025 00:27:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a123e0891df9257f803cbe743e03c02d15c183ad2b8cacd65fd9f4f2dabb0`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac6ec0e0a081338e2cbb451bffdaca705d2a4f0fe7583434d7ef8b6e47ab7f`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b2976226ef7e4240d6d5de076fd3b5bbcb43eca8b57c1d163112ee7a56299`  
		Last Modified: Wed, 12 Nov 2025 01:18:14 GMT  
		Size: 362.9 MB (362901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7cf76df497daac8b3723be228a8b22dd260d20c211984a6cad34d2cb982cfe`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732238e2700dd5d584f610b90293aa3ec4e2ba1dfc254749b65979a76ce19a5`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd423cf81614bb4043f2c29fca28ae32fd185e499132924d96777bfa50dd40c`  
		Last Modified: Wed, 12 Nov 2025 00:28:30 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:8a1ac54400c70c6214c39175babc24b9eae8edf59fb3f9588d664849cd264150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75711de4ab8ca7e926c1d8e2cabdc7e5d64c414a9fefe08ade5d6a7c38e1b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:cb60fd4c5e2a76a908212955768b70e9900ad3c8b3b26f4f41b6586dbebf8499`  
		Last Modified: Wed, 12 Nov 2025 03:10:19 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:524f00b7f07ca3e7bfc11966670e1aaed0970643397bdab20ea7769b4912c147
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:724d8c85b87825e6974c70601e149f83f9c22546ad462a3874927ac2f9643d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254934054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdd0707d4ea971dff5a171d9e3621360e9711b3d3bb1314ca94062873231d70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:32 GMT
ENV PSMDB_VERSION=6.0.25-20
# Wed, 12 Nov 2025 00:27:32 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:32 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Wed, 12 Nov 2025 00:27:32 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:32 GMT
ENV PSMDB_REPO=release
# Wed, 12 Nov 2025 00:27:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:32 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:32 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:46 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:46 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:46 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1c54392d147d3dfab6ca19a27327785c56b93195979b88d0ea0c21546eca7`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 8.7 MB (8730491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cdb08967d72819688a84870d957ebed51b4c8df7eb078bb2ba4770d80fc993`  
		Last Modified: Wed, 12 Nov 2025 03:11:04 GMT  
		Size: 205.2 MB (205249986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56555a1f0ce9559833a00681351e797038bceb374a65a136182b588c614f47`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d33227ab1ada6f54758273944866a47bfe756c8c7a9cc89d206ee86ba2f96`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1292f47409adf84c7e4bac9075f5f58d6cbe54c2b29f07885a2684cabfbad00`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b355801c944d3b918c8354eb8d760dad3ddbf764d9d31796a2de16913247`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1a28431a866bfea3a79a0236d58663e6056810ac17e9325ce280303d4b5d4e`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba61d018778ce3d8d6c61292840dc0acf3ef27adfe3fbb1eeb9857b21ee07c2`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e962d5b4b79d3f3809d503eec44a1490f35a0a5e688e2a7ea937fc77f0adb1b`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:d8ac5ff28c7efbcfb1632245819b643302a678d22a3e573928b07fcd2e64c9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de37ca77d76eb2a149ba9b702961b71e62153645e50b091ca1b2cfb4d19f92dd`

```dockerfile
```

-	Layers:
	-	`sha256:a1f20e5c9f83cbd777c27bea0a36639b9474dc62b04ac868ab4f61bcc75dd55d`  
		Last Modified: Wed, 12 Nov 2025 03:10:36 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.25`

```console
$ docker pull percona@sha256:524f00b7f07ca3e7bfc11966670e1aaed0970643397bdab20ea7769b4912c147
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.25` - linux; amd64

```console
$ docker pull percona@sha256:724d8c85b87825e6974c70601e149f83f9c22546ad462a3874927ac2f9643d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254934054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdd0707d4ea971dff5a171d9e3621360e9711b3d3bb1314ca94062873231d70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:32 GMT
ENV PSMDB_VERSION=6.0.25-20
# Wed, 12 Nov 2025 00:27:32 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:32 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Wed, 12 Nov 2025 00:27:32 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:32 GMT
ENV PSMDB_REPO=release
# Wed, 12 Nov 2025 00:27:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:32 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:32 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:43 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:46 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:46 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:46 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1c54392d147d3dfab6ca19a27327785c56b93195979b88d0ea0c21546eca7`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 8.7 MB (8730491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cdb08967d72819688a84870d957ebed51b4c8df7eb078bb2ba4770d80fc993`  
		Last Modified: Wed, 12 Nov 2025 03:11:04 GMT  
		Size: 205.2 MB (205249986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56555a1f0ce9559833a00681351e797038bceb374a65a136182b588c614f47`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d33227ab1ada6f54758273944866a47bfe756c8c7a9cc89d206ee86ba2f96`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1292f47409adf84c7e4bac9075f5f58d6cbe54c2b29f07885a2684cabfbad00`  
		Last Modified: Wed, 12 Nov 2025 00:28:18 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b355801c944d3b918c8354eb8d760dad3ddbf764d9d31796a2de16913247`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1a28431a866bfea3a79a0236d58663e6056810ac17e9325ce280303d4b5d4e`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba61d018778ce3d8d6c61292840dc0acf3ef27adfe3fbb1eeb9857b21ee07c2`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e962d5b4b79d3f3809d503eec44a1490f35a0a5e688e2a7ea937fc77f0adb1b`  
		Last Modified: Wed, 12 Nov 2025 00:28:19 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.25` - unknown; unknown

```console
$ docker pull percona@sha256:d8ac5ff28c7efbcfb1632245819b643302a678d22a3e573928b07fcd2e64c9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de37ca77d76eb2a149ba9b702961b71e62153645e50b091ca1b2cfb4d19f92dd`

```dockerfile
```

-	Layers:
	-	`sha256:a1f20e5c9f83cbd777c27bea0a36639b9474dc62b04ac868ab4f61bcc75dd55d`  
		Last Modified: Wed, 12 Nov 2025 03:10:36 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:49da5c2f1d0ff6208ab8d0941413403e3dee9cd523bcc0f37a076e551c58e650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:c3cceddef1ba1ce4e8ab2304a4d687711ca1e0133cc6431c43cbf6c6223e3133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277119508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f482c47d6f78b37f3a3a0ab1250d4c74fd2fdb18c48cbca6d9aa33331a5e0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:31 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_VERSION=7.0.24-13
# Wed, 12 Nov 2025 00:27:31 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_REPO=release
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:31 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:49 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:49 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:49 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73047587270686922d1191755775878f752dc1a59856d65b828c32688832d5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:26 GMT  
		Size: 8.7 MB (8727515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ff091975087827a474fa57edde54716e48be8a0a8124168bd87b0c78fcbe2`  
		Last Modified: Wed, 12 Nov 2025 03:11:01 GMT  
		Size: 227.4 MB (227438400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3231a789ed402b1d063f3df933f3fce05f7ad24c06462133e3df609833cecb2`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57318a81affc0ac28852e2a70e059a1d4ebb64d5b1e048422d267739512cbc02`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9664e1a9b7104c44dcc7885bf832f8b7489bc8c21a91d455cc04b89216d18`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9597d36374a952897128affbe7c7cdfe2ac0e19e356a12cb9ff7746ace9c1259`  
		Last Modified: Wed, 12 Nov 2025 00:28:26 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba609abefd65b045e0ff587fa69bc3e67c81ceb26e0a4aff5540b1110bf5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37bca44c98c670092a0cf6853a32deb1a4282f07abf762e580486a22ec37eeb`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efb3647cc71b67092c77c324abe5a60c4acb25b77a51348e404020d39ee6866`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:8c53a860c4a2ffc7c039e348a74276ba5e96ffd81586772958dbe01a2b26fa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ffe3b495fc98a5c64de383a055e16d58583176f7473805946f9e79379087ce`

```dockerfile
```

-	Layers:
	-	`sha256:e80016fa98d1fbd8b4dd30d2a1991d6a01fe7c20d97b217db0da5d509e5015d4`  
		Last Modified: Wed, 12 Nov 2025 03:10:44 GMT  
		Size: 32.3 KB (32284 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.24`

```console
$ docker pull percona@sha256:49da5c2f1d0ff6208ab8d0941413403e3dee9cd523bcc0f37a076e551c58e650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.24` - linux; amd64

```console
$ docker pull percona@sha256:c3cceddef1ba1ce4e8ab2304a4d687711ca1e0133cc6431c43cbf6c6223e3133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277119508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f482c47d6f78b37f3a3a0ab1250d4c74fd2fdb18c48cbca6d9aa33331a5e0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:31 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_VERSION=7.0.24-13
# Wed, 12 Nov 2025 00:27:31 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_REPO=release
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:31 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:47 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:49 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:49 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:49 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73047587270686922d1191755775878f752dc1a59856d65b828c32688832d5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:26 GMT  
		Size: 8.7 MB (8727515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ff091975087827a474fa57edde54716e48be8a0a8124168bd87b0c78fcbe2`  
		Last Modified: Wed, 12 Nov 2025 03:11:01 GMT  
		Size: 227.4 MB (227438400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3231a789ed402b1d063f3df933f3fce05f7ad24c06462133e3df609833cecb2`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57318a81affc0ac28852e2a70e059a1d4ebb64d5b1e048422d267739512cbc02`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9664e1a9b7104c44dcc7885bf832f8b7489bc8c21a91d455cc04b89216d18`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9597d36374a952897128affbe7c7cdfe2ac0e19e356a12cb9ff7746ace9c1259`  
		Last Modified: Wed, 12 Nov 2025 00:28:26 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba609abefd65b045e0ff587fa69bc3e67c81ceb26e0a4aff5540b1110bf5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37bca44c98c670092a0cf6853a32deb1a4282f07abf762e580486a22ec37eeb`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efb3647cc71b67092c77c324abe5a60c4acb25b77a51348e404020d39ee6866`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.24` - unknown; unknown

```console
$ docker pull percona@sha256:8c53a860c4a2ffc7c039e348a74276ba5e96ffd81586772958dbe01a2b26fa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ffe3b495fc98a5c64de383a055e16d58583176f7473805946f9e79379087ce`

```dockerfile
```

-	Layers:
	-	`sha256:e80016fa98d1fbd8b4dd30d2a1991d6a01fe7c20d97b217db0da5d509e5015d4`  
		Last Modified: Wed, 12 Nov 2025 03:10:44 GMT  
		Size: 32.3 KB (32284 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:c24a04a7dc2687f1c20f23469c3aaa50f612621c7e45e2e7b3ddc4320508acca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:1399e2ce1388c7e1a164aad1e8c3161b9c132ac7672806fe96f2acb69dbca889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292658210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c949d954be6d88d4319d1287a4e15c86f1b95b408677bc74835de9ab33b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:31 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_VERSION=8.0.12-4
# Wed, 12 Nov 2025 00:27:31 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_REPO=testing
# Wed, 12 Nov 2025 00:27:31 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:31 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:49 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:49 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:49 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c4a637669385a0e1fb2b3bfd6ffc96ecd857f06d70c250e7ff5421e452b8e`  
		Last Modified: Wed, 12 Nov 2025 00:28:29 GMT  
		Size: 8.7 MB (8727557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b938da05a6df43cedfeb44e78d01882ea5d7991e1a8054c7c89ab59add54483c`  
		Last Modified: Wed, 12 Nov 2025 03:11:08 GMT  
		Size: 243.0 MB (242977070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c1123dcc564d6ab81d1c6f9e163de6b2c47a91b472a5d2a346b4f81bdf2d15`  
		Last Modified: Wed, 12 Nov 2025 00:28:23 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5793bdb1ccdf859942d43af1644d9b65dc83e70bf3f255e610000dd02ce7fbb7`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf8b7a233360efce4e0f797572c2d3ea265362ce078769d7c5bd0f6084fe43`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f6dfd2592232ab1e98c9d3e00ad911003e71c8f6bf199fc72617ea30604f9`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba609abefd65b045e0ff587fa69bc3e67c81ceb26e0a4aff5540b1110bf5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a20b84e8cc31e40e0b4ab0511833aa46c1cf438b5b51a8e3c48bbfdd6d8007`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad370e42cd8858eb89848fb655eef00954163425a8e61a539335c8b3454b525`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:177d485f6bc9dd7a35f800174ae48930b5966817bdfcbc25edf1887dbb240b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a563e032b086ba8645580ce6a7d9059308f3704344fa3f249e917093583cc7`

```dockerfile
```

-	Layers:
	-	`sha256:6777ffe546b3776fe54fc18f86bfaa3f3e645108e6a447725714d5ef9a8dc1e8`  
		Last Modified: Wed, 12 Nov 2025 03:10:50 GMT  
		Size: 32.6 KB (32574 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.12`

```console
$ docker pull percona@sha256:c24a04a7dc2687f1c20f23469c3aaa50f612621c7e45e2e7b3ddc4320508acca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.12` - linux; amd64

```console
$ docker pull percona@sha256:1399e2ce1388c7e1a164aad1e8c3161b9c132ac7672806fe96f2acb69dbca889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292658210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c949d954be6d88d4319d1287a4e15c86f1b95b408677bc74835de9ab33b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:31 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Nov 2025 00:27:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_VERSION=8.0.12-4
# Wed, 12 Nov 2025 00:27:31 GMT
ENV OS_VER=el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Wed, 12 Nov 2025 00:27:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV PSMDB_REPO=testing
# Wed, 12 Nov 2025 00:27:31 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 12 Nov 2025 00:27:31 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 12 Nov 2025 00:27:31 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 12 Nov 2025 00:27:46 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
VOLUME [/data/db]
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 12 Nov 2025 00:27:48 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 12 Nov 2025 00:27:49 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:49 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 12 Nov 2025 00:27:49 GMT
USER 1001
# Wed, 12 Nov 2025 00:27:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c4a637669385a0e1fb2b3bfd6ffc96ecd857f06d70c250e7ff5421e452b8e`  
		Last Modified: Wed, 12 Nov 2025 00:28:29 GMT  
		Size: 8.7 MB (8727557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b938da05a6df43cedfeb44e78d01882ea5d7991e1a8054c7c89ab59add54483c`  
		Last Modified: Wed, 12 Nov 2025 03:11:08 GMT  
		Size: 243.0 MB (242977070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c1123dcc564d6ab81d1c6f9e163de6b2c47a91b472a5d2a346b4f81bdf2d15`  
		Last Modified: Wed, 12 Nov 2025 00:28:23 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5793bdb1ccdf859942d43af1644d9b65dc83e70bf3f255e610000dd02ce7fbb7`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf8b7a233360efce4e0f797572c2d3ea265362ce078769d7c5bd0f6084fe43`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f6dfd2592232ab1e98c9d3e00ad911003e71c8f6bf199fc72617ea30604f9`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba609abefd65b045e0ff587fa69bc3e67c81ceb26e0a4aff5540b1110bf5e`  
		Last Modified: Wed, 12 Nov 2025 00:28:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a20b84e8cc31e40e0b4ab0511833aa46c1cf438b5b51a8e3c48bbfdd6d8007`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad370e42cd8858eb89848fb655eef00954163425a8e61a539335c8b3454b525`  
		Last Modified: Wed, 12 Nov 2025 00:28:24 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.12` - unknown; unknown

```console
$ docker pull percona@sha256:177d485f6bc9dd7a35f800174ae48930b5966817bdfcbc25edf1887dbb240b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a563e032b086ba8645580ce6a7d9059308f3704344fa3f249e917093583cc7`

```dockerfile
```

-	Layers:
	-	`sha256:6777ffe546b3776fe54fc18f86bfaa3f3e645108e6a447725714d5ef9a8dc1e8`  
		Last Modified: Wed, 12 Nov 2025 03:10:50 GMT  
		Size: 32.6 KB (32574 bytes)  
		MIME: application/vnd.in-toto+json
