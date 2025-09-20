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
