## `percona:ps-8.0`

```console
$ docker pull percona@sha256:b331cf296a131e6986d61f0198c2ebee27ea44fd086db7b4ad8140b54a9bd6ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:9ff71489eb91925959f8c7e37e20ed6dfc94059f89022611bb593f0807eb0d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369327317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f40d2b52fd60683ab4da23db9826f85947aa87387ef2de30f2f139590e891c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Feb 2025 04:20:08 GMT
ENV container oci
# Thu, 13 Feb 2025 04:20:08 GMT
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Thu, 13 Feb 2025 04:20:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Feb 2025 04:20:08 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:20:08 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 13 Feb 2025 04:20:12 GMT
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
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 05:39:37 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 05:39:36 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c2e9212fc533a0ca0ccb67064d3108a61c1ba09eede6f0a5d7520a58ddbed`  
		Last Modified: Wed, 26 Feb 2025 20:28:46 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5f07c7d3a90eac69f0cd9dfca52ce58fd11abfe61974efb9615755d7d9b91c`  
		Last Modified: Wed, 26 Feb 2025 20:28:46 GMT  
		Size: 8.3 MB (8322684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5a65f3eb0ed1cc23ccbc9c0a54595fa208217c6a5f3a5e6ab8b69cc8c8120d`  
		Last Modified: Wed, 26 Feb 2025 20:28:51 GMT  
		Size: 321.6 MB (321627892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b38f63016599e99bb4fc73ea722ef36c777902bad03de03e222ea337f80597`  
		Last Modified: Wed, 26 Feb 2025 20:28:46 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00687a1cf5d7f47e29d5f420d0443c344badfdaf9bc7244143ed4dc270d54062`  
		Last Modified: Wed, 26 Feb 2025 20:28:47 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f2630ab8a752870866c3d5e8d9bbfa9f1bdc466d768591c74b7c4470576fb8`  
		Last Modified: Wed, 26 Feb 2025 20:28:47 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:1b6e22db3bb92628420a3e1860a31b49c7e541d2f52077bfecc5dcac73c8dc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b9bdcc401fffa90e34b190037072b3d0d4b22ecc445f1288c1335c7fcb91c`

```dockerfile
```

-	Layers:
	-	`sha256:973a94816c6518303ff9c99641a0aa9974b75dad49742232beb5bfdcf177a0e7`  
		Last Modified: Wed, 26 Feb 2025 20:28:46 GMT  
		Size: 31.9 KB (31926 bytes)  
		MIME: application/vnd.in-toto+json
