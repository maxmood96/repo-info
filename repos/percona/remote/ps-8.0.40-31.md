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
		Last Modified: Thu, 06 Feb 2025 05:31:07 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:31:05 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b257c8507e7d4889bfaf2e1277668f1331dd0a18c33db52dee56c2e46861646`  
		Last Modified: Fri, 07 Feb 2025 00:28:36 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd57124556264e8dffbae1078e070467c9e106af6e92167487f03fb0d5d516`  
		Last Modified: Fri, 07 Feb 2025 00:28:37 GMT  
		Size: 8.3 MB (8335572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125370866e9ca0d6dcf6c2b55e6be79ebbdb4be8007585029741f1c181b7f84c`  
		Last Modified: Fri, 07 Feb 2025 00:28:45 GMT  
		Size: 338.2 MB (338155135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4809fc4e99b9a212647b7eea51a410e9ec08609901b3814fe5d1f71dac089d0`  
		Last Modified: Fri, 07 Feb 2025 00:28:37 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c848b1eb095ed04febe46b1fc67f32bc05d286074e70a32aa30bcb107ede0`  
		Last Modified: Fri, 07 Feb 2025 00:28:38 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4a9c6ed7d94f78d220c1ca12ad8e07e45f79c698bcf169dba750b3f9b8b2c`  
		Last Modified: Fri, 07 Feb 2025 00:28:38 GMT  
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
		Last Modified: Fri, 07 Feb 2025 00:28:36 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json
