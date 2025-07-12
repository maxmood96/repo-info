## `percona:ps-8`

```console
$ docker pull percona@sha256:ad4ff0d8bb922d0a7fca9349a9e8264024f36e6f6bca44888ae54b78bcdc9017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:0a83b0e863d04633986c98d4167cb204cfa56117e61700367d5888bd0d018e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431033347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a5408128c15a8628415e0c5644a5e561618f281e9dcad57ff28248b5b0513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e714fc75eee3b673cf0bf3a501b7b11acd520fc7e79c0b18d31ba31e24c929c`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb73c7e62e7e7f294bda328d4a0832532718c420bdc15fbb75de54bb8975aa`  
		Last Modified: Fri, 11 Jul 2025 23:34:38 GMT  
		Size: 8.9 MB (8857810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0ece68540ba44e4d1a2ecf7d36b57abf51986ab14139ca12536964a915297`  
		Last Modified: Sat, 12 Jul 2025 02:10:53 GMT  
		Size: 382.5 MB (382509025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1b599c2e1a5cf7bb94b4e2b92be7eca1f067517c3df102937cabeaee22062`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64582a41cab030838d9befcc3ce2fb03e00ff4c73c8e82cd8b4b6b934ca16301`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071d04d37182184117881fbbd8a90ec768b3af7b3d06322b38490f642c44d5b`  
		Last Modified: Fri, 11 Jul 2025 23:34:37 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:778b689ab6953b21f60891bf80dcb43b649daa473617c731e991a1bb61fdbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237d34d1004c0d0e75f9ad0746cd972814e0646e292344cc073beb77ab58624`

```dockerfile
```

-	Layers:
	-	`sha256:133ae5c4560b01b9fb96df621b9fb69a4fbe615abef9a59eb01cbdc0e3244b76`  
		Last Modified: Sat, 12 Jul 2025 02:10:18 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json
