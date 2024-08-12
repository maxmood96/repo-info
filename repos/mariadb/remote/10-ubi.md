## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:18e16406d39b96169fcc260ef11e3ab2455d3444f98b0541e70a3cf795bd1683
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:10-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:24c15d9494f874f66aa837ba807fcc94aef525f6bd3bbffda2c02cdb270f8e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145350088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75834ffd86cf7729fa8c3c41d88e89aeb880767151fd59df82a53399b002d977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:41 GMT
ADD file:87021d55df71c4e3f216afb8a8fafe806663072c4406db403bba88d029cd4114 in / 
# Thu, 18 Jul 2024 16:00:41 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:41 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:42 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:42 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:42 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:42 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:43 GMT
ADD file:5044c31992c75e94cf041ad1beda86a0b218ead5785a55734e242465ef7798db in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:43 GMT
ADD file:97862c9bc77fad8fca444d897df1eb9d08bd77f12f61288c39c576743736d49f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:43 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:44 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:44 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.9 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
USER mysql
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:247c2d03e9487628cb6754ff5385a670df160f7bba36af8fc1f2066e461dc36e`  
		Last Modified: Tue, 23 Jul 2024 23:20:51 GMT  
		Size: 38.9 MB (38868726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6dd2529f4a101bfc12ca70ba5a8e54a3f2cc5aebb49bb6bbfcd80f1755519`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f5f5d36ccfcb389d9e0d0eb3382fe4dc403483033fd007f2d241661f9b705a`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 983.5 KB (983470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03f1a58e88295e16fefe3d7918a8061a2a885b24e66fba47bc7aa08afbefad4`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0fdfa7a85281de257e064713d30e678b7f599a351d5f9e7e1048498bded297`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d499ba6c6cf6ce58d88e89e4b4e74d3a32eefb0a36b9d11b6232d15b8e217b1d`  
		Last Modified: Mon, 12 Aug 2024 16:56:47 GMT  
		Size: 105.5 MB (105484025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6113bd8331b75ea45de3a9f80088a1f94bda73679fffcd087d8a5d603218ad22`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2709dbbfbd3bbcdf1c625b89681107a344639d298b8b26bcd3f8178818c36707`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673383c129357c1728e292e86e02e151df0de00bf92a80d748b2aba604f1bd8`  
		Last Modified: Mon, 12 Aug 2024 16:56:45 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:3cef59d713c5f8b3a748fd06afd6b429aa4b7df382694a0aed726b04541e7681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baa0cc4452b8c453109b37fd95c7473da172912184fdc7079c52ce47162b6fd`

```dockerfile
```

-	Layers:
	-	`sha256:cab1ec0957811d90302ceb4761fb6b8d98b925c39e226905893f0e907882ef98`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 3.9 MB (3918610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8eedecbdebca1772a9c1e9d195f0fc516c51452b1972b5356b815c20acc0e8`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 30.2 KB (30164 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0537e7b23de69fa748ab3fb4796a8fae71ce8bed4bab590bd4fdb9e578f3ad07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141847845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffb63ac033ef636b7b58ed1f43276b34dfce28b309391523e9f387837748a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:25 GMT
ADD file:f709fba0574079e9aa46a5b75f6fc5d799887bd4f82a7be2013a2e4437ff041f in / 
# Thu, 18 Jul 2024 16:00:27 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:27 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:27 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:27 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:27 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:29 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:c9f3c26999c1ebf7b158f6d526405f4f2a7761aeaf3986c120c5ba32f61b0820 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:ba00fa3144a82bce8698247481dc2415535fa14e5557f1639e90fdfa9c65461d in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:30 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:32 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:34 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.9 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
USER mysql
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:63c76be6b13c3916a86a82fe30d0c63bde321c804abe11ea9f3bae73f5832bdf`  
		Last Modified: Tue, 23 Jul 2024 23:20:54 GMT  
		Size: 37.1 MB (37072383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a80c17a00050830c2cb67972c6d8336c5fcd6f51499e4cb94e97b454917cd57`  
		Last Modified: Wed, 24 Jul 2024 23:00:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9d689981fec0b12316bb46ef88644b103a588960c4adf8936492da2e0201b`  
		Last Modified: Wed, 24 Jul 2024 23:00:54 GMT  
		Size: 913.8 KB (913813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903a6d85e81247c3a9597847237c322bf6167d68a6d7ec822ae0f66a33439faa`  
		Last Modified: Wed, 24 Jul 2024 23:03:05 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8636efaead5ec6a2e1e81f0a8bafaaba78654efdf4e1dd2416f8237ebae707`  
		Last Modified: Wed, 24 Jul 2024 23:03:05 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c5734e89b0fe6d1c07485c34d83607409cb511f854f3c0eb665f8690971501`  
		Last Modified: Mon, 12 Aug 2024 17:07:00 GMT  
		Size: 103.8 MB (103847787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d2d94d07a99e6f59ab535c84633a4476e4b361d82327cfd164400db390accb`  
		Last Modified: Mon, 12 Aug 2024 17:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b6c0fc26678965ff6eff3bc20cef4e5aa874b85a81c4e746c8c5e114bdc8f`  
		Last Modified: Mon, 12 Aug 2024 17:06:58 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e783936f3e95361be3d63d24b51719fce324a31c78c7f73b4f2cd6eddecc027`  
		Last Modified: Mon, 12 Aug 2024 17:06:58 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:cccc7230b527ac5e00b25c87a969bd94ed1ffaf83ae536d450709dd31491ba9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51dd81bb30cb532601102b32c833967cd9bfe14a55ed495440f50f51cdb342`

```dockerfile
```

-	Layers:
	-	`sha256:3a0164f5a7c1c02e0ce26060ecbf9926753f786ccdb379ea90b56d7c8a48dc00`  
		Last Modified: Mon, 12 Aug 2024 17:06:58 GMT  
		Size: 3.9 MB (3918556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae753c4c7bc08c2ae5bdac2e001da7644adbcd307c953d78cc950efb1e65f691`  
		Last Modified: Mon, 12 Aug 2024 17:06:58 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:efa1140902c8df14217d2174dfc171a2933b67a0370364a48681b4d3d05f5222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155789453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d43f248de2a55e7d5ff9dbe31c840934c1018b978e2b305c97ed1d303ec5c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:28 GMT
ADD file:506188f12e028f4115fb2ba353f364678bbb8ea8c5ec9b669f44281addfd1c23 in / 
# Thu, 18 Jul 2024 16:00:29 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:29 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:29 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:29 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:30 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:30 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:31 GMT
ADD file:3f6d24259ae37b294276696c5e5ca3f2dcb0aad9637655ed1e08e29dbfc6190c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:31 GMT
ADD file:3a81328001d719dfa2946d3215c3dd6d6a01bef72303dd878a79d9b8d46b2979 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:31 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:35 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.9 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
USER mysql
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a7d93ea5d89e1a76516910d4ef69c80d2186bf11033dd5d398ced6ab61a80eb`  
		Last Modified: Wed, 24 Jul 2024 00:09:48 GMT  
		Size: 43.3 MB (43310938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc198f614bdf78cc9aea8fc7dec97b241dc14fc7f42c03fb1676c83a3c05d1fe`  
		Last Modified: Thu, 25 Jul 2024 03:04:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d903b254a7487ab6ca42f586d08d6b3a338afc57ec4a3758306c4b1a3f5f29`  
		Last Modified: Thu, 25 Jul 2024 03:04:10 GMT  
		Size: 904.3 KB (904314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bc47b21948cd629ea69fe50c252050f172c9396d11994256e2c0f165e98651`  
		Last Modified: Thu, 25 Jul 2024 03:08:01 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804f5ac05dc96da3de7b76fca8fb37674bd1f9d18542f51ed7363573f314d94`  
		Last Modified: Thu, 25 Jul 2024 03:08:01 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b25a86bc5232b9e9fd0d1d223aa752bfcf64b6f10af781d63a4ae10f0d71f5`  
		Last Modified: Mon, 12 Aug 2024 17:11:24 GMT  
		Size: 111.6 MB (111560332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1283b95952117defb3a73e0511157cd76f0a497e5a561a33f49c580aced829`  
		Last Modified: Mon, 12 Aug 2024 17:11:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bef02c5a705cfeeea729e609e091aad965ad30037ec9c0e18588eff55049e19`  
		Last Modified: Mon, 12 Aug 2024 17:11:20 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d89aea759f02b8c1497ccf8a7c6aa6866cae89b4e40d9746ca71d289ddbd85`  
		Last Modified: Mon, 12 Aug 2024 17:11:20 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:3ca70fe72a31210fdf31bed16add61286576c39f81f5e1ef15536bf4101c90fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136106328fb1c3cf752f27b788f0903701880cc18decff1bf112fe7f580bff9b`

```dockerfile
```

-	Layers:
	-	`sha256:9170ff95345ed628413aac63f667a23c2ee89f6bf68cad7aaad854411d1c56af`  
		Last Modified: Mon, 12 Aug 2024 17:11:20 GMT  
		Size: 3.9 MB (3919796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcdbbbdcd20d5ae40871e22b218a495ea5a11cc1f9d71bccd76129cf83ebf86`  
		Last Modified: Mon, 12 Aug 2024 17:11:20 GMT  
		Size: 30.2 KB (30221 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:e352d9042535f2bfa3e367ba35c99bad86bf8b10dfade6e849939df095e05387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144030923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8953fd9cad3916d79a0c793156f619701cf71529bd9d80a47012ace4d549e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 18 Jul 2024 16:02:12 GMT
ADD file:1a0498fcbd53ea6a4cce5caa1a166c86ab5a3d63fb2e6f1005f6229cd3fd8ddc in / 
# Thu, 18 Jul 2024 16:02:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:02:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:02:13 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:02:13 GMT
ENV container oci
# Thu, 18 Jul 2024 16:02:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:02:13 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:02:14 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:02:14 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:260b735774b29b332765c57758623137b24eea7dfd0749ddc4f622d177cc9a81 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:6c5a2a1a67a074079cab4ce304a1b74e6ebbcec0d31479580388db97c242c818 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:02:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:02:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:02:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:02:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.9 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=10.11.9
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=10.11.9
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
USER mysql
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:503bb890315f555a5f9d7cf50d5a90a092481d25c9c474822b5e12c758ad6065`  
		Last Modified: Wed, 24 Jul 2024 00:09:55 GMT  
		Size: 37.1 MB (37116517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbebd451e119879a09a6aa60279428060c459d57f90308f10cf7783411b208`  
		Last Modified: Wed, 24 Jul 2024 23:08:21 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8efe4d18a77b5920f5f179a24ba5573d7d0d2dda45775676ca65ae30926f76`  
		Last Modified: Wed, 24 Jul 2024 23:08:21 GMT  
		Size: 948.1 KB (948119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f0abfa49c855ed99aea1da7fcb8650e41f2b66ce6f3d6b527854af0131296`  
		Last Modified: Wed, 24 Jul 2024 23:10:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508c1da7a8c7c43927f8e6b5d41d9cc2b4b9736dc0115be84071ad8b96e6c86`  
		Last Modified: Wed, 24 Jul 2024 23:10:51 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d752f9ed0134941a9c077ceb23cd91c8c2664760c6c2ad66fbbfbf7b4ac7156e`  
		Last Modified: Mon, 12 Aug 2024 17:12:53 GMT  
		Size: 106.0 MB (105952420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a243fc7ed4a021f06c031ee5ec7a9a63bb486240770d79693bfd63409c60525`  
		Last Modified: Mon, 12 Aug 2024 17:12:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d546fb983d68947a91b6d61dad8700dc8a1c30ab13196e10533a1e8ea0e152`  
		Last Modified: Mon, 12 Aug 2024 17:12:51 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3457be7d05997728b7f9ba08518c30f94b7f59d8a39c816fcafa26c094a6d48`  
		Last Modified: Mon, 12 Aug 2024 17:12:51 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:19b33ec9eadfcfeff4a8909390c8d5b05fd97914ee358a84ec1597c545e41d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc2cdf10d8ba682df63503dfce48884fc7f2bd3bcf3ed7f6f6a8c62fea9e77e`

```dockerfile
```

-	Layers:
	-	`sha256:f598b96e615f3c04978ea0e1de410af0b4d3f7234159e866b970d916aed74034`  
		Last Modified: Mon, 12 Aug 2024 17:12:51 GMT  
		Size: 3.9 MB (3919781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b970eaeea8c22f78f4464734f5f069b0e09785fb415e3b665c605239767eec8`  
		Last Modified: Mon, 12 Aug 2024 17:12:51 GMT  
		Size: 30.2 KB (30165 bytes)  
		MIME: application/vnd.in-toto+json
