<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.40-31`](#percona8040-31)
-	[`percona:8.0.40-31-centos`](#percona8040-31-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.40-31`](#perconaps-8040-31)
-	[`percona:psmdb-5.0`](#perconapsmdb-50)
-	[`percona:psmdb-5.0.29`](#perconapsmdb-5029)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.19`](#perconapsmdb-6019)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.15`](#perconapsmdb-7015)

## `percona:8`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.40-31`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.40-31` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.40-31` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.40-31-centos`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.40-31-centos` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.40-31-centos` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.40-31`

```console
$ docker pull percona@sha256:7f9f2938c22150f54c88a337c2962ebc6fd46fe7dda456da72cff8a298850049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.40-31` - linux; amd64

```console
$ docker pull percona@sha256:316829f76c08ca47d00ed93ee74263b5d150754672b7ba1e9d8451d7b516f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385871166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77a330f973be29ef8afadc106fc3fd0c00b759adc712c2e2f5fd132dc4fea8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 03:10:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 03:10:26 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 03:11:31 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 03:10:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 03:10:27 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 03:11:22 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.40-31` - unknown; unknown

```console
$ docker pull percona@sha256:7662774b2e1f4b2ef6b00c4fe62038d89df458e76674b4b6663800d17a12c981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fafa3cbbc0c2d5263d6d130af2db47bf270a91d7198f576bf8d1dae6026b5c`

```dockerfile
```

-	Layers:
	-	`sha256:a03e94a33a5b619a92abc26f729ca4c3612d3337499c1d1e001bc714e970b05e`  
		Last Modified: Fri, 07 Feb 2025 03:45:16 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:4458a7fd7d52e1fff00d6da71b07b6f1176aa4993334e0b8d4cbd028bf2803c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:9c9e0ddbe43cd64b3c5879d1b515521ec1a82f06de0b930a5c9fe1ce3e28424c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.9 MB (259921427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edc7dba4e2f3fc064cf813327046c18fe65fba28eb85d4dfcc0f3767d68e3bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=5.0.29-25
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=5.0.29-25.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ec61f6666626da4cb445316f8ef40d85d251f82d8a74a7579e3bde0f386d1`  
		Last Modified: Thu, 13 Feb 2025 10:48:08 GMT  
		Size: 4.3 MB (4304964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cadaa151690bc9e7696a8d36ea21ee5b6c1bfded3d076f2fb34feb861861882`  
		Last Modified: Wed, 12 Feb 2025 02:56:31 GMT  
		Size: 153.9 MB (153884099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecce2b5b7ff54749daa359b0755823df2701a4bac5258d84a924b31c9d478ab6`  
		Last Modified: Thu, 13 Feb 2025 10:48:06 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695bb2f5c0962bed294e67be842a1428f932cc0b00b503588f435912ad5a32e`  
		Last Modified: Tue, 11 Feb 2025 06:10:41 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d7afee888d10cc052733d3b62bc3442d9590c2404858a5849a1d9ab16ce5c`  
		Last Modified: Wed, 12 Feb 2025 02:55:36 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507b2abbcb4c2d05262cf0c6743743bb221c740ae8175f3f2fdadd390d52e14c`  
		Last Modified: Wed, 12 Feb 2025 02:55:38 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ef86f662ca216c905aded5140f1ead507bdf67ed8c18d97c428d62bfcd45fe`  
		Last Modified: Thu, 13 Feb 2025 10:48:09 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca43b9cc5cbff9778e8b60ded8379dd87069782b4cc08e19c6d7b05caf33d82`  
		Last Modified: Wed, 12 Feb 2025 02:55:40 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f858aaf96b9238aafad6a1c06611d2822d4cae632b0b471027e4b3da46633cee`  
		Last Modified: Tue, 11 Feb 2025 06:10:42 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-5.0` - unknown; unknown

```console
$ docker pull percona@sha256:97809dec7aa85509472e45ab080c62e462ba85538ad6bc5c2bda896e4b9b3142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5374b3bdbed9633212e2e732609ee8da37a4f1625a3f6355bd6dbc333a67ead9`

```dockerfile
```

-	Layers:
	-	`sha256:c2065b0c7fd681015b5895a575b1baf097b229bfe59b34ca82373f8c84ad8d62`  
		Last Modified: Mon, 10 Feb 2025 20:09:14 GMT  
		Size: 32.2 KB (32189 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-5.0.29`

```console
$ docker pull percona@sha256:4458a7fd7d52e1fff00d6da71b07b6f1176aa4993334e0b8d4cbd028bf2803c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-5.0.29` - linux; amd64

```console
$ docker pull percona@sha256:9c9e0ddbe43cd64b3c5879d1b515521ec1a82f06de0b930a5c9fe1ce3e28424c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.9 MB (259921427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edc7dba4e2f3fc064cf813327046c18fe65fba28eb85d4dfcc0f3767d68e3bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=5.0.29-25
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=5.0.29-25.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ec61f6666626da4cb445316f8ef40d85d251f82d8a74a7579e3bde0f386d1`  
		Last Modified: Thu, 13 Feb 2025 10:48:08 GMT  
		Size: 4.3 MB (4304964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cadaa151690bc9e7696a8d36ea21ee5b6c1bfded3d076f2fb34feb861861882`  
		Last Modified: Wed, 12 Feb 2025 02:56:31 GMT  
		Size: 153.9 MB (153884099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecce2b5b7ff54749daa359b0755823df2701a4bac5258d84a924b31c9d478ab6`  
		Last Modified: Thu, 13 Feb 2025 10:48:06 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695bb2f5c0962bed294e67be842a1428f932cc0b00b503588f435912ad5a32e`  
		Last Modified: Tue, 11 Feb 2025 06:10:41 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d7afee888d10cc052733d3b62bc3442d9590c2404858a5849a1d9ab16ce5c`  
		Last Modified: Wed, 12 Feb 2025 02:55:36 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507b2abbcb4c2d05262cf0c6743743bb221c740ae8175f3f2fdadd390d52e14c`  
		Last Modified: Wed, 12 Feb 2025 02:55:38 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ef86f662ca216c905aded5140f1ead507bdf67ed8c18d97c428d62bfcd45fe`  
		Last Modified: Thu, 13 Feb 2025 10:48:09 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca43b9cc5cbff9778e8b60ded8379dd87069782b4cc08e19c6d7b05caf33d82`  
		Last Modified: Wed, 12 Feb 2025 02:55:40 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f858aaf96b9238aafad6a1c06611d2822d4cae632b0b471027e4b3da46633cee`  
		Last Modified: Tue, 11 Feb 2025 06:10:42 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-5.0.29` - unknown; unknown

```console
$ docker pull percona@sha256:97809dec7aa85509472e45ab080c62e462ba85538ad6bc5c2bda896e4b9b3142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5374b3bdbed9633212e2e732609ee8da37a4f1625a3f6355bd6dbc333a67ead9`

```dockerfile
```

-	Layers:
	-	`sha256:c2065b0c7fd681015b5895a575b1baf097b229bfe59b34ca82373f8c84ad8d62`  
		Last Modified: Mon, 10 Feb 2025 20:09:14 GMT  
		Size: 32.2 KB (32189 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:5015b4b455d8e64e275c003be8f775a025e78488c943e7a10e21fe4c2270bb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:d5e58d72da7a195a63575f8ed4227aeca608b45baa7b0c5670d4717ee9dd0d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295311267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354b4f82174e577b9ad67b916af6f82028f1fe62e307a335ed70958e7f8961a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=6.0.19-16
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=6.0.19-16.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f3d00e35d280f8e6790e0b5bcb5acd4c519511bbc99b992d76cb3b887fd10`  
		Last Modified: Wed, 12 Feb 2025 02:54:58 GMT  
		Size: 4.3 MB (4304967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e868c197abbc10d74eb6e0cbdb16c2c8e065cbdf6d235ac7ff616fcb2d884f`  
		Last Modified: Tue, 11 Feb 2025 09:00:04 GMT  
		Size: 189.3 MB (189273932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8498aaa052b902ce99b02fd049c2863365813986bab7d6aa04766750bb51f9`  
		Last Modified: Wed, 12 Feb 2025 02:54:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5e207b992d16d9b599156bb2ac0a7182064f8070d7695a1508a7ac163c096b`  
		Last Modified: Tue, 11 Feb 2025 09:00:08 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f23d9c16d13e4d79444835fe48d247a69c829388984db4ef2cae93deef38c9a`  
		Last Modified: Tue, 11 Feb 2025 09:00:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e136d1ec47ac0d8bb1963c055b6d99609562f3e9a0da9d521a8baa090a572d`  
		Last Modified: Wed, 12 Feb 2025 02:54:07 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591e7c926ca148bb3dd7124e08155a837a8d64e4e52b53142225141538a8cbb`  
		Last Modified: Thu, 13 Feb 2025 10:25:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff0cf791cc199541325779a06f9b93ec3ecf18670973923ebdd5a3a77e5352`  
		Last Modified: Tue, 11 Feb 2025 09:00:09 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f3747674a413d90197939a9285a419a3d010d7c8c73bb72993d6e8f0fc5a0`  
		Last Modified: Thu, 13 Feb 2025 10:25:43 GMT  
		Size: 4.8 KB (4832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:1f267dab0887cd6d36026454f797a6f11443e40c071b361f9d875b3c214fdf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815605479cd6834a8bed673aaf7ebfed6fd8c579646deb89003b683df9bdd188`

```dockerfile
```

-	Layers:
	-	`sha256:d118cc48b91cf99efbef02ecdb1040dd9df23cf8600c651cd959d0272d1cdd98`  
		Last Modified: Tue, 11 Feb 2025 08:59:37 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.19`

```console
$ docker pull percona@sha256:5015b4b455d8e64e275c003be8f775a025e78488c943e7a10e21fe4c2270bb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.19` - linux; amd64

```console
$ docker pull percona@sha256:d5e58d72da7a195a63575f8ed4227aeca608b45baa7b0c5670d4717ee9dd0d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295311267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354b4f82174e577b9ad67b916af6f82028f1fe62e307a335ed70958e7f8961a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=6.0.19-16
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=6.0.19-16.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f3d00e35d280f8e6790e0b5bcb5acd4c519511bbc99b992d76cb3b887fd10`  
		Last Modified: Wed, 12 Feb 2025 02:54:58 GMT  
		Size: 4.3 MB (4304967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e868c197abbc10d74eb6e0cbdb16c2c8e065cbdf6d235ac7ff616fcb2d884f`  
		Last Modified: Tue, 11 Feb 2025 09:00:04 GMT  
		Size: 189.3 MB (189273932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8498aaa052b902ce99b02fd049c2863365813986bab7d6aa04766750bb51f9`  
		Last Modified: Wed, 12 Feb 2025 02:54:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5e207b992d16d9b599156bb2ac0a7182064f8070d7695a1508a7ac163c096b`  
		Last Modified: Tue, 11 Feb 2025 09:00:08 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f23d9c16d13e4d79444835fe48d247a69c829388984db4ef2cae93deef38c9a`  
		Last Modified: Tue, 11 Feb 2025 09:00:09 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e136d1ec47ac0d8bb1963c055b6d99609562f3e9a0da9d521a8baa090a572d`  
		Last Modified: Wed, 12 Feb 2025 02:54:07 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591e7c926ca148bb3dd7124e08155a837a8d64e4e52b53142225141538a8cbb`  
		Last Modified: Thu, 13 Feb 2025 10:25:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff0cf791cc199541325779a06f9b93ec3ecf18670973923ebdd5a3a77e5352`  
		Last Modified: Tue, 11 Feb 2025 09:00:09 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f3747674a413d90197939a9285a419a3d010d7c8c73bb72993d6e8f0fc5a0`  
		Last Modified: Thu, 13 Feb 2025 10:25:43 GMT  
		Size: 4.8 KB (4832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.19` - unknown; unknown

```console
$ docker pull percona@sha256:1f267dab0887cd6d36026454f797a6f11443e40c071b361f9d875b3c214fdf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815605479cd6834a8bed673aaf7ebfed6fd8c579646deb89003b683df9bdd188`

```dockerfile
```

-	Layers:
	-	`sha256:d118cc48b91cf99efbef02ecdb1040dd9df23cf8600c651cd959d0272d1cdd98`  
		Last Modified: Tue, 11 Feb 2025 08:59:37 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:35c58fcbd5bee77a6dc1a4854c07c5be9411f72ea9faa40955c601be9d4d5cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:39b17f81c4d83529764dadae13557b768649f180157db8d0dd8864ef13780a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306804032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e416969f5eba49437b02c0313ff0181d3700703efa02194e57e81ee870b6cdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=7.0.15-9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=7.0.15-9.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4df3f03973c33db0cfd6d367ac46424aee62aeed19024bd6881d3d0fe86994a`  
		Last Modified: Wed, 12 Feb 2025 07:04:53 GMT  
		Size: 4.3 MB (4304942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073f0feca80bb56832c667090270131221c1b097929f981d8b568dd247815792`  
		Last Modified: Wed, 12 Feb 2025 02:53:04 GMT  
		Size: 200.8 MB (200766716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae8e5e5c74ad0487fe2583c2a4765e1e38393d4fbbd93ed6d113b1f8c7ee19`  
		Last Modified: Wed, 12 Feb 2025 02:52:56 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9613c8fe0754f04cb9e75fe3a5b59f38c17e703d9f9e685aa47a77630a1bd7d`  
		Last Modified: Mon, 10 Feb 2025 21:10:21 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f979a64d4b21c8c7e061ec7326800545e10a92f9e08d51e452427f813ea739`  
		Last Modified: Tue, 11 Feb 2025 06:35:06 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0507d7eaed3aaf3a3d527eefa605b10bbe77c2c34acb2332ef33522ffade4603`  
		Last Modified: Thu, 13 Feb 2025 10:03:15 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700b4b9a82c14aa2737f3a09dea989053ad9775269625dfc91ea8fc9432044dc`  
		Last Modified: Tue, 11 Feb 2025 06:35:08 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf4316dcf091bac4f33295d909f452ed94d0b9234670133e8b108a138783830`  
		Last Modified: Thu, 13 Feb 2025 10:03:16 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba4bdf6ee32549a62a1456ef9c2201aec660960e93f7f6becc4780174c7fad3`  
		Last Modified: Mon, 10 Feb 2025 21:10:21 GMT  
		Size: 4.8 KB (4837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:2344b33ee1dbbf47bc82a6cdfe527087d7ff9125c844bcafb99bbae77dbb722f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1860e71642ba406d1a9311105f23bd75c96a994b4be13f06aab50c8e4b93402`

```dockerfile
```

-	Layers:
	-	`sha256:d17d3489addb9e00e190943628de987ee13329ad9b5c040b334a3384fdddef1b`  
		Last Modified: Mon, 10 Feb 2025 20:09:28 GMT  
		Size: 32.2 KB (32215 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.15`

```console
$ docker pull percona@sha256:35c58fcbd5bee77a6dc1a4854c07c5be9411f72ea9faa40955c601be9d4d5cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.15` - linux; amd64

```console
$ docker pull percona@sha256:39b17f81c4d83529764dadae13557b768649f180157db8d0dd8864ef13780a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306804032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e416969f5eba49437b02c0313ff0181d3700703efa02194e57e81ee870b6cdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=7.0.15-9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=7.0.15-9.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f30d2f906615ac2c482a15c4d3e5b16fdb9b9a93ab5175d18afef9d1777af5c9`  
		Last Modified: Mon, 10 Feb 2025 21:23:31 GMT  
		Size: 100.8 MB (100779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4df3f03973c33db0cfd6d367ac46424aee62aeed19024bd6881d3d0fe86994a`  
		Last Modified: Wed, 12 Feb 2025 07:04:53 GMT  
		Size: 4.3 MB (4304942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073f0feca80bb56832c667090270131221c1b097929f981d8b568dd247815792`  
		Last Modified: Wed, 12 Feb 2025 02:53:04 GMT  
		Size: 200.8 MB (200766716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae8e5e5c74ad0487fe2583c2a4765e1e38393d4fbbd93ed6d113b1f8c7ee19`  
		Last Modified: Wed, 12 Feb 2025 02:52:56 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9613c8fe0754f04cb9e75fe3a5b59f38c17e703d9f9e685aa47a77630a1bd7d`  
		Last Modified: Mon, 10 Feb 2025 21:10:21 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f979a64d4b21c8c7e061ec7326800545e10a92f9e08d51e452427f813ea739`  
		Last Modified: Tue, 11 Feb 2025 06:35:06 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0507d7eaed3aaf3a3d527eefa605b10bbe77c2c34acb2332ef33522ffade4603`  
		Last Modified: Thu, 13 Feb 2025 10:03:15 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700b4b9a82c14aa2737f3a09dea989053ad9775269625dfc91ea8fc9432044dc`  
		Last Modified: Tue, 11 Feb 2025 06:35:08 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf4316dcf091bac4f33295d909f452ed94d0b9234670133e8b108a138783830`  
		Last Modified: Thu, 13 Feb 2025 10:03:16 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba4bdf6ee32549a62a1456ef9c2201aec660960e93f7f6becc4780174c7fad3`  
		Last Modified: Mon, 10 Feb 2025 21:10:21 GMT  
		Size: 4.8 KB (4837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.15` - unknown; unknown

```console
$ docker pull percona@sha256:2344b33ee1dbbf47bc82a6cdfe527087d7ff9125c844bcafb99bbae77dbb722f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1860e71642ba406d1a9311105f23bd75c96a994b4be13f06aab50c8e4b93402`

```dockerfile
```

-	Layers:
	-	`sha256:d17d3489addb9e00e190943628de987ee13329ad9b5c040b334a3384fdddef1b`  
		Last Modified: Mon, 10 Feb 2025 20:09:28 GMT  
		Size: 32.2 KB (32215 bytes)  
		MIME: application/vnd.in-toto+json
