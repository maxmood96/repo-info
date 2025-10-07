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
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34-centos`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34-centos` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34-centos` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.43-34`

```console
$ docker pull percona@sha256:5821d42e628779d4fae69d4a8fdb62cb2d91ecf5621d692c4d2dcac2348c8409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:d490f9531d48e44d49dba3c02cbb4ac60f04677a57eae525cfef6950d9bb5748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410899934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e097f131de2ffd1609ab3db8677a6c2499af764c26cc34fde8f3c2ef29ec76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfacc749e57c46c95917faa7c53a458584d1c4de6609a1591d4989afb6ae990`  
		Last Modified: Fri, 19 Sep 2025 20:39:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98350e7b54745f6792727d5321692129827ef8a93e5cc39d08a0006e3e2a7ec7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 8.9 MB (8860556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d104aadd1aa48c7d99fd7c978dc8f3e5261dab9c8c26e0b486540b490f6438`  
		Last Modified: Fri, 19 Sep 2025 21:17:00 GMT  
		Size: 362.4 MB (362381395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e5d57169ccb17643d578bfd1016bac0b73185840024d12e3da1e5975d731c`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ffb8fd16148623b920ddf14a2243b397952d8dd440a989209f4a8bf186beba`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461307c73ea08aaf3f84ec8b3135ae1913995693d13400f7f96d9753ba33eca7`  
		Last Modified: Fri, 19 Sep 2025 20:39:51 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:4053705620d7bc3e04a032e6603cd3b1baa5e0f0cd6b2eb068acb2130a16ae75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326fbc53b853ecfaa9e7c2858d1094bba25a34bb571a742cec42775d36b94c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed8355b8cc26c3d002be7af6b6f094915d90f9d0f4c2ab293adbf5fa1e35034b`  
		Last Modified: Fri, 19 Sep 2025 23:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:95ee3cec2c9a7d452e4daa9531262c81b84c9d2a43cfeccd64066934ef4dbb43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:5ca396ce1e4a2eb7ff348a66a4a35d4a02cf2089c5d623b94d83fbaea4f4931f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254149272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce773961a30287342f0ca8d23ec94553dd131167642e44b9cbec6f7a55f97b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:26:55 GMT
ENV container oci
# Fri, 01 Aug 2025 11:26:55 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 01 Aug 2025 11:26:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=6.0.25-20
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_REPO=release
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 01 Aug 2025 11:26:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
VOLUME [/data/db]
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 01 Aug 2025 11:26:55 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Aug 2025 11:26:55 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 01 Aug 2025 11:26:55 GMT
USER 1001
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28797c2e8401bfc6dc626396eccf860225851bcb64ac4ad1b3bfcca570af4120`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 8.5 MB (8489945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c954cf0985939c3921014ac2a11bc843436f61f537634b58b4e0959d4f96756`  
		Last Modified: Sun, 21 Sep 2025 00:14:08 GMT  
		Size: 205.1 MB (205058227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a3c9ac6390387bc1f861bfc8efbd10c6c8dc83e49e8ef62e66ae0940794764`  
		Last Modified: Fri, 19 Sep 2025 20:41:15 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc4944e3f8b794cdc7ab8bb5ffc24ad28d738a97db254aa71cc1abd4065097b`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7259c510994f5bbae87f93d93e710ed1f167b28b5ed79103b85f4d2b6c4b96`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d444a33d9e7f02cc50e2a00d0b79dded0ca1f88698c6239f2760b1470f00100`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5d57d093f29825dedb4e220583208e4bb45a102e8afe8f0e2f7eb6437cb8a`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61e490d131906902d9d844615a6ac1f39aba20ad96c8b5763c4da8705f1bcd`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 4.0 KB (3962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e254ac05351230b400bb340d4c0055d8aa5756f067790a0395bc4f69b543f7`  
		Last Modified: Fri, 19 Sep 2025 20:41:18 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:1c5c249148299eaea7b7a0e0e69df5d60ef330abf3fbfae858b09ebb4eb13256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d0334bf60dc2fc64b9f6e2fc40a72affd2d3643f6c19bad5de6dbb24875079`

```dockerfile
```

-	Layers:
	-	`sha256:9d0acebe78f221eccbb9a357bf8aa2e8c709db9b3854581ddf64b868d3b9413a`  
		Last Modified: Fri, 19 Sep 2025 23:10:37 GMT  
		Size: 32.8 KB (32761 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.25`

```console
$ docker pull percona@sha256:95ee3cec2c9a7d452e4daa9531262c81b84c9d2a43cfeccd64066934ef4dbb43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.25` - linux; amd64

```console
$ docker pull percona@sha256:5ca396ce1e4a2eb7ff348a66a4a35d4a02cf2089c5d623b94d83fbaea4f4931f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254149272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce773961a30287342f0ca8d23ec94553dd131167642e44b9cbec6f7a55f97b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:26:55 GMT
ENV container oci
# Fri, 01 Aug 2025 11:26:55 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 01 Aug 2025 11:26:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=6.0.25-20
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_REPO=release
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 01 Aug 2025 11:26:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
VOLUME [/data/db]
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 01 Aug 2025 11:26:55 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Aug 2025 11:26:55 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 01 Aug 2025 11:26:55 GMT
USER 1001
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28797c2e8401bfc6dc626396eccf860225851bcb64ac4ad1b3bfcca570af4120`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 8.5 MB (8489945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c954cf0985939c3921014ac2a11bc843436f61f537634b58b4e0959d4f96756`  
		Last Modified: Sun, 21 Sep 2025 00:14:08 GMT  
		Size: 205.1 MB (205058227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a3c9ac6390387bc1f861bfc8efbd10c6c8dc83e49e8ef62e66ae0940794764`  
		Last Modified: Fri, 19 Sep 2025 20:41:15 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc4944e3f8b794cdc7ab8bb5ffc24ad28d738a97db254aa71cc1abd4065097b`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7259c510994f5bbae87f93d93e710ed1f167b28b5ed79103b85f4d2b6c4b96`  
		Last Modified: Fri, 19 Sep 2025 20:41:16 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d444a33d9e7f02cc50e2a00d0b79dded0ca1f88698c6239f2760b1470f00100`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5d57d093f29825dedb4e220583208e4bb45a102e8afe8f0e2f7eb6437cb8a`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61e490d131906902d9d844615a6ac1f39aba20ad96c8b5763c4da8705f1bcd`  
		Last Modified: Fri, 19 Sep 2025 20:41:17 GMT  
		Size: 4.0 KB (3962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e254ac05351230b400bb340d4c0055d8aa5756f067790a0395bc4f69b543f7`  
		Last Modified: Fri, 19 Sep 2025 20:41:18 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.25` - unknown; unknown

```console
$ docker pull percona@sha256:1c5c249148299eaea7b7a0e0e69df5d60ef330abf3fbfae858b09ebb4eb13256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d0334bf60dc2fc64b9f6e2fc40a72affd2d3643f6c19bad5de6dbb24875079`

```dockerfile
```

-	Layers:
	-	`sha256:9d0acebe78f221eccbb9a357bf8aa2e8c709db9b3854581ddf64b868d3b9413a`  
		Last Modified: Fri, 19 Sep 2025 23:10:37 GMT  
		Size: 32.8 KB (32761 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:446f030311fe367409da0834e5aee56dd6917accc0677eb499cf624081f1ecf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:d947402a9f074f6e3e4ac8e877a9c56159070b12a5828ea4b64f04cd5d15b9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276239456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40929d04ab7dda77b63a142ddca6d663ab4a1827a753f2eadd47316605b2353`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=7.0.24-13
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=release
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021eb52bd505473a29845a29d28668a7b0a5d28372fdbc5fbcdfda931040eab6`  
		Last Modified: Tue, 07 Oct 2025 17:40:04 GMT  
		Size: 8.4 MB (8399682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509a2e7efb1140d4dc3e13a478b7b8f4b54805b834435a71a6093bf67d5a8606`  
		Last Modified: Tue, 07 Oct 2025 17:42:40 GMT  
		Size: 227.2 MB (227238675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56ab1e6e10febc471781db1fb4fd7a390a4d667d504448fdcf7ede3aa11e95`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5e1fc594a2b79ca5f345e0bd4995570df1c80efd48c61af3f853a6c93854c6`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a43d9a3164d8d905c1b93c5cc9c1c2801307d9888f03be6516847fa042890`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871919971354b7dc23b8c0174536b776cd522e77c1bbdbccfd2ec66bfc3b2296`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7863b88d91e3b29cefe6d45f4b446f76fc66cc7579ea1b096d8babdd57be7d32`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14e55e7186428a9cd3eb998fd24e98728e6e05e460acaf7c558e2c39585d40c`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853e2eb450fb546d03f977798587af7d6f4caa2c6af37df3d8fb001115954ac`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:5ec0fd260e5aa74654eb50e7df3c6098f7661e27f1abc14f92b8271cfa0bd78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace5321b734d9973810c48a9b9f1a0f8be99c6ef72f7233e358c28d7a9852d5`

```dockerfile
```

-	Layers:
	-	`sha256:2ee0387bd7f5f4c6681445c5dd0a25fedc5927a7f65e4aa19625ee517cb02dfd`  
		Last Modified: Tue, 07 Oct 2025 20:10:21 GMT  
		Size: 32.3 KB (32268 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.24`

```console
$ docker pull percona@sha256:446f030311fe367409da0834e5aee56dd6917accc0677eb499cf624081f1ecf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.24` - linux; amd64

```console
$ docker pull percona@sha256:d947402a9f074f6e3e4ac8e877a9c56159070b12a5828ea4b64f04cd5d15b9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276239456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40929d04ab7dda77b63a142ddca6d663ab4a1827a753f2eadd47316605b2353`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=7.0.24-13
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=release
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021eb52bd505473a29845a29d28668a7b0a5d28372fdbc5fbcdfda931040eab6`  
		Last Modified: Tue, 07 Oct 2025 17:40:04 GMT  
		Size: 8.4 MB (8399682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509a2e7efb1140d4dc3e13a478b7b8f4b54805b834435a71a6093bf67d5a8606`  
		Last Modified: Tue, 07 Oct 2025 17:42:40 GMT  
		Size: 227.2 MB (227238675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56ab1e6e10febc471781db1fb4fd7a390a4d667d504448fdcf7ede3aa11e95`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5e1fc594a2b79ca5f345e0bd4995570df1c80efd48c61af3f853a6c93854c6`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a43d9a3164d8d905c1b93c5cc9c1c2801307d9888f03be6516847fa042890`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871919971354b7dc23b8c0174536b776cd522e77c1bbdbccfd2ec66bfc3b2296`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7863b88d91e3b29cefe6d45f4b446f76fc66cc7579ea1b096d8babdd57be7d32`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14e55e7186428a9cd3eb998fd24e98728e6e05e460acaf7c558e2c39585d40c`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853e2eb450fb546d03f977798587af7d6f4caa2c6af37df3d8fb001115954ac`  
		Last Modified: Tue, 07 Oct 2025 17:39:21 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.24` - unknown; unknown

```console
$ docker pull percona@sha256:5ec0fd260e5aa74654eb50e7df3c6098f7661e27f1abc14f92b8271cfa0bd78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace5321b734d9973810c48a9b9f1a0f8be99c6ef72f7233e358c28d7a9852d5`

```dockerfile
```

-	Layers:
	-	`sha256:2ee0387bd7f5f4c6681445c5dd0a25fedc5927a7f65e4aa19625ee517cb02dfd`  
		Last Modified: Tue, 07 Oct 2025 20:10:21 GMT  
		Size: 32.3 KB (32268 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:f36a3ebab210daa632bbde4cd5bc5afc06d9c14b52d68a9042b45d7744bf6a9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:b490c371eeaf5ca8437ed6a7a050101fb042117a58e55ac2d6557e28ddbbf0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e4e4daf7617a1774076fe813340f28cf5a5ecf2d6af6e0bfc38acbd63e9ffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021eb52bd505473a29845a29d28668a7b0a5d28372fdbc5fbcdfda931040eab6`  
		Last Modified: Tue, 07 Oct 2025 17:40:04 GMT  
		Size: 8.4 MB (8399682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e7f1dd101e987e4077ef276705f2ff6810149a3ac3bfaf20d1d2fd5b1ef478`  
		Last Modified: Tue, 07 Oct 2025 17:42:48 GMT  
		Size: 242.8 MB (242776634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fe7f88df839c72691ef0ceb177d0d4959ca0178de823aa08901b9352f591c`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0777d50ad30d696b10d4b9d27c1cc8304e883b8b735b94667c6b3aba9859f4`  
		Last Modified: Tue, 07 Oct 2025 17:39:39 GMT  
		Size: 4.1 KB (4068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e9533d29d09a1ddebf1f1d5b028695cae0d417298face1ea42bbbbbab2292`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189c5ddf25c6c7c0b30fa8dd7a8866be30a321435301cce27f7107412748f1d`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc8a7716413630d771ae98b8399416b956110f7ef8c037528e258a88138a739`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cdb0f89aa77f2376c18ef1bd730c83afa684ec82e228145471c83a63f1ec4c`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91bfebc81c3e3d29b9c7c157a1a7932d0020a3dae99d861a1c71d346faeb7ad`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:e3482dfb5a6eea7a402812669b5d00e9cfff07616e06a0b6a4b62fb8916e285c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c173fdc041e4bf6297a4eaf578fb0b0f9d110537eea7b921edd85ef9573d1`

```dockerfile
```

-	Layers:
	-	`sha256:7335b79ea424f2164901cb20e39944fceed2dea8a00cc83aefb57c819b4f07ed`  
		Last Modified: Tue, 07 Oct 2025 20:10:27 GMT  
		Size: 32.6 KB (32558 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.12`

```console
$ docker pull percona@sha256:f36a3ebab210daa632bbde4cd5bc5afc06d9c14b52d68a9042b45d7744bf6a9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.12` - linux; amd64

```console
$ docker pull percona@sha256:b490c371eeaf5ca8437ed6a7a050101fb042117a58e55ac2d6557e28ddbbf0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e4e4daf7617a1774076fe813340f28cf5a5ecf2d6af6e0bfc38acbd63e9ffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021eb52bd505473a29845a29d28668a7b0a5d28372fdbc5fbcdfda931040eab6`  
		Last Modified: Tue, 07 Oct 2025 17:40:04 GMT  
		Size: 8.4 MB (8399682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e7f1dd101e987e4077ef276705f2ff6810149a3ac3bfaf20d1d2fd5b1ef478`  
		Last Modified: Tue, 07 Oct 2025 17:42:48 GMT  
		Size: 242.8 MB (242776634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fe7f88df839c72691ef0ceb177d0d4959ca0178de823aa08901b9352f591c`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0777d50ad30d696b10d4b9d27c1cc8304e883b8b735b94667c6b3aba9859f4`  
		Last Modified: Tue, 07 Oct 2025 17:39:39 GMT  
		Size: 4.1 KB (4068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e9533d29d09a1ddebf1f1d5b028695cae0d417298face1ea42bbbbbab2292`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189c5ddf25c6c7c0b30fa8dd7a8866be30a321435301cce27f7107412748f1d`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc8a7716413630d771ae98b8399416b956110f7ef8c037528e258a88138a739`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cdb0f89aa77f2376c18ef1bd730c83afa684ec82e228145471c83a63f1ec4c`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91bfebc81c3e3d29b9c7c157a1a7932d0020a3dae99d861a1c71d346faeb7ad`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.12` - unknown; unknown

```console
$ docker pull percona@sha256:e3482dfb5a6eea7a402812669b5d00e9cfff07616e06a0b6a4b62fb8916e285c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c173fdc041e4bf6297a4eaf578fb0b0f9d110537eea7b921edd85ef9573d1`

```dockerfile
```

-	Layers:
	-	`sha256:7335b79ea424f2164901cb20e39944fceed2dea8a00cc83aefb57c819b4f07ed`  
		Last Modified: Tue, 07 Oct 2025 20:10:27 GMT  
		Size: 32.6 KB (32558 bytes)  
		MIME: application/vnd.in-toto+json
