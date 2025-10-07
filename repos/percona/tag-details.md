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
$ docker pull percona@sha256:c1679b54b5ec8743fecff9f71dcaa742fc6971ab4b7674ef9aa40b1fe4717412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:261f980d48f52b5907b4b33a8e48e2c147dd9cbbe979ae1c6fadd469e34f0986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274506560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f86448bbb59509f3d583c030a4f9a6b668d5c69ec5d0a052d4104b71b8c47a`
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
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=7.0.22-12
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=7.0.22-12.el9
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
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:27427513ac8657e57aa800d57f430de235543dba0f633e6c8b2b234adf005509`  
		Last Modified: Fri, 19 Sep 2025 20:40:52 GMT  
		Size: 8.5 MB (8486593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052b14c614612d8409c0c2f2c6a97a8b8215a72781d5efaa669c35a25525b05a`  
		Last Modified: Fri, 19 Sep 2025 23:12:05 GMT  
		Size: 225.4 MB (225418867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8686a8ffaeae7cec39d69e542d2f6e69087a6e5bc2e13a769766eea7bc6d7787`  
		Last Modified: Fri, 19 Sep 2025 20:40:51 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58731d5797ccd81668a81166287e53eb9a4764ba7846c8ebea058406003afd51`  
		Last Modified: Fri, 19 Sep 2025 20:40:52 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d46211a4b0112d4b0462ae116d4d9c5990148b2c409ca71fabbe0229aeba427`  
		Last Modified: Fri, 19 Sep 2025 20:40:52 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675fcef475f582983c2b9a5057034b7478cfb9292f8138c0a9bd9030adaf647`  
		Last Modified: Fri, 19 Sep 2025 20:40:52 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9779b59ad9a9aa27fcc16f76d82e17b8a0884332a32c1bfd93ec3a17e21ad7f`  
		Last Modified: Fri, 19 Sep 2025 20:40:54 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe5b8534f327c65c1081a919e41f0d635e076f42ca4d487f708470568d78e4`  
		Last Modified: Fri, 19 Sep 2025 20:40:54 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9a59a1bebed951a3431d24f70b77a250d76d6bcf19b36a5a08a8e8b61a0c9`  
		Last Modified: Fri, 19 Sep 2025 20:40:54 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:b74698a1fdf74febd18826350a8e345e2b04371d2972b02e3ff91f798f6b8db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdcfbad953b07a7f1bf8ce8bbe003b25204bb9a9c11c94f7ec9929b7ca8ae9a`

```dockerfile
```

-	Layers:
	-	`sha256:1f565b5f489ff08bd32e7607f53ab5239c60cf01738c1c328fef2ff0200eea84`  
		Last Modified: Fri, 19 Sep 2025 23:10:44 GMT  
		Size: 32.3 KB (32268 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.24`

**does not exist** (yet?)

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:3e8dcbe56673c3d97654a846d7ff5bea2f4319598b36832598701780b249d68d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:45dcd1d103cb6a67378c50e1694b6bd9e70c7cfbfc5ee30d83b1645a08b9050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290322424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c23e583b0aeedb1d72b43f55daf1ed5622b137734c0d7e85fae68c4b345e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
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
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
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
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e8bb0683bb6d493c26b201e8ef5ed95b1534afc099e2c92be6aa6cb3f067ee`  
		Last Modified: Fri, 19 Sep 2025 20:40:53 GMT  
		Size: 8.5 MB (8486579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2243d5ddcf7dba5f9341d0fe40bcfa1191bc0e545ba7c7be183343a7ebb6b`  
		Last Modified: Fri, 19 Sep 2025 23:12:05 GMT  
		Size: 241.2 MB (241234750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b0b9b64e6a3578d14351e290016ebcedef093a1992bc95826920d7ae14581`  
		Last Modified: Fri, 19 Sep 2025 20:40:50 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b607d88f7114698b517be8654c21b84947c747dfe1f6f3af849d64872f89ff`  
		Last Modified: Fri, 19 Sep 2025 20:40:50 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abee76ff5aac7244daf6013da552d7ce13da9cffc7aeecb2890c57d2e642f3be`  
		Last Modified: Fri, 19 Sep 2025 20:40:50 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2db4c9d76bb72b0b97b4f384c39cea1b82897014c93a7da558e900024ed5e3`  
		Last Modified: Fri, 19 Sep 2025 20:40:51 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8deb305ad9a96fc5a761b4e51722ad9cccee57da638b4efc5628233c4177ae1`  
		Last Modified: Fri, 19 Sep 2025 20:40:50 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b571b99ddb514a102b416700968dae867e0483d7a8a974c1983eac7702136f8`  
		Last Modified: Fri, 19 Sep 2025 20:40:50 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea001ba943ad4a930dd04be4021013d34e9a9bacf161378310081113c2ed9c7`  
		Last Modified: Fri, 19 Sep 2025 20:40:51 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:c9479fadf9529eeff7c746fe0659209cbe2e26f083c2cebc06490822868dc8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e91ee03021e1e11ff91a28cb9a073dda0648b681579787f5dd5b93000e4d1b2`

```dockerfile
```

-	Layers:
	-	`sha256:8152c7dacb0dac10e6f34d511672164e947c5a3a6a380294027b224468fb1bed`  
		Last Modified: Fri, 19 Sep 2025 23:10:51 GMT  
		Size: 32.4 KB (32436 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.12`

**does not exist** (yet?)
