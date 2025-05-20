## `percona:ps-8`

```console
$ docker pull percona@sha256:05e6499b0e535ae2b3bd67145af27562e928ad3f1a65105b6374960724ee3f7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:7314309ed7f7553cf309663e609a91d30f7282bb29caa9de67e3a6756657811d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 MB (430717287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964c160f638cb239cda8bbef1e62eee4debbfd18e94798e8d4d70392ff93ee7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 May 2025 10:36:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:36:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:36:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:36:11 GMT
ENV container oci
# Wed, 14 May 2025 10:36:11 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Wed, 14 May 2025 10:36:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:36:11 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:36:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:36:12 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Wed, 14 May 2025 14:33:02 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57258cf8c015b4ff095cd76db4b60b6fc5dd751a63d2fb1f405bb6c24a1d800`  
		Last Modified: Mon, 19 May 2025 23:14:16 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7d69c6f111255b47ae2668198a2f55f923304c8af8f5c43aa67b92203826d`  
		Last Modified: Mon, 19 May 2025 23:14:17 GMT  
		Size: 8.9 MB (8858148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf267aee0ceff781d52f204c4289440b5b665edbe436ad4d86cf7b4ca8eaf5`  
		Last Modified: Mon, 19 May 2025 23:14:28 GMT  
		Size: 382.2 MB (382204315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cdbff359054900b38da62ea852286cca7281222ebc9b466cb3792d1e8aeae4`  
		Last Modified: Mon, 19 May 2025 23:14:17 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e160b2de755642a277cfb3896b33427dbaa230f3060bd4619ee9b06d317200d`  
		Last Modified: Mon, 19 May 2025 23:14:18 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275076e129739cd1e62fda00037813a1a3b140718a3a7ad4ca6198ea0424cf6`  
		Last Modified: Mon, 19 May 2025 23:14:18 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:2bad223a1cfa23c3654fc38736a37cde1174b3a43ebbcc2c9ff032029970ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dd3907e4f65c34433ac32df81019fd4cb93cdbb3d9196b9f7800d7074fe000`

```dockerfile
```

-	Layers:
	-	`sha256:19b46a517757983b992c51c7037228238e1b944b0ae6a348effe422d6f1c6bc0`  
		Last Modified: Mon, 19 May 2025 23:14:17 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json
