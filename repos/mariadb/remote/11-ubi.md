## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:bd1af14ef4e4fbc791edecabd89524da013e61eaf01fce834a8943217c38f027
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

### `mariadb:11-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:3916d4b548e830d68698ac642c47d59fb1c94cfd8fd1bfff17a60a84270022bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145735573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9805e8aab7709c04c17f69d183beab758624275bf32ed34d81e7800726ab3ca`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
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
	-	`sha256:b411f31673b4d4fe3ae469868e89be9230c842eb289a4d14722c095a5bf59c70`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc01ae45216884614af7dd780771c5bb2b8f8e09ef2b706a9c3f156b92e072e`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 983.5 KB (983470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d377dcf180387c639b287301062d7927d53da84353242a4fa6dde9e2c9976ed9`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e889d27a08226018033f172171a87803a182a702ac3813831f585137ae118d`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40269f1d99b334eddd7fd3930d06e63b6070d3d195c8886b1b632152877c97d`  
		Last Modified: Mon, 12 Aug 2024 16:56:33 GMT  
		Size: 105.9 MB (105869451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2709efa92ba15aad3d304c99514ee3cba93960d0c008b9c09b4881db9133cb8c`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731a75340d22b8dfe9b0610959c16b1857ebc9b5b6a34fad2af00cb73a7fdb85`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e846335c7a7ac81bd1b3737a854b16edc19b28389e52dd3386c68c3edc1ce7`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:251c0e643589d5b39f29f4a34edbb43e9ee372566e14f85aa535f30bd3b39bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37631d1033b791c15d4f8771eddea6e6617aef1d1fda9bcc18545ec891943bfe`

```dockerfile
```

-	Layers:
	-	`sha256:e67a7205e903c21ded76c4cb0cdc33548efbc6b356ec788fc023e2d47ef25eff`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 3.9 MB (3922167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9e369855286cc85c08f31c9181cb83559a65671e89718597ec84f0c9d17ad1`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a2b16f80a49d93637a72e5d724c3feafbb554f7e2ab752cdf8c37b823d98ff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142219135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ef8a65771a1db4afffe9c49a00040bee17c8d864a4764e6c1ff2d92f0cd8b`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
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
	-	`sha256:24f711f63269a10a4afe17fc62a0c3e01d8fbaced48431c058dcb09c9996f9b3`  
		Last Modified: Mon, 12 Aug 2024 17:01:05 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834eae704a863ebe301277ab13c69a8857c5c4eb6ca598883370f478e76fc74`  
		Last Modified: Mon, 12 Aug 2024 17:01:05 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a98d2ddf7660182c87dd1641ac9051d274c56282f5f17c9d2047e26afb18c4d`  
		Last Modified: Mon, 12 Aug 2024 17:01:10 GMT  
		Size: 104.2 MB (104219006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4584241895d4f9f6a05de36733c9c3e8d3d6bda0407f4516526c26497975b2`  
		Last Modified: Mon, 12 Aug 2024 17:01:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb694f2df33e99a62cdc5d2d0fa483cd3c7cd2efdff490368fbcf1c38e30de`  
		Last Modified: Mon, 12 Aug 2024 17:01:06 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6923aa7327339656a5d915e42fcf413db63d8b4cbf2686ac6d0ca36e2920f26d`  
		Last Modified: Mon, 12 Aug 2024 17:01:06 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:312f39350fdfb23d5b684a9eae06f4e1d5fcedc7d6c169cf5901055500437b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f22593a359a6690f69483a944761b2692cf2a83ccb62948b21b652550cf9b`

```dockerfile
```

-	Layers:
	-	`sha256:cc40e8c14cb9b7f8ccb61a9c47070b5590b7c13eaa549d2e5dec1acd88e28249`  
		Last Modified: Mon, 12 Aug 2024 17:01:05 GMT  
		Size: 3.9 MB (3922137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de78ec046d14f1512dd0e6543bd798966d0d9f998d0854594f9679053ea6519`  
		Last Modified: Mon, 12 Aug 2024 17:01:05 GMT  
		Size: 31.1 KB (31109 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c551529f4ef226d141729c206815ed985c0748f78981b67de04917c3506d0ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156210457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe2bee080cf7ddff057ac9f0dee717a030453ad72d5e43e2aee4b0ca19e1d2a`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
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
	-	`sha256:23e723cac7936d1313fae9338ea0d1fb45bb8a86d6e1af55d1a475c185609ce2`  
		Last Modified: Mon, 12 Aug 2024 17:02:00 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9977a5a93aeb59d7c517464570f4b6dd312fcaf0d6c387def321c855723fdb76`  
		Last Modified: Mon, 12 Aug 2024 17:02:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7da0115bf489c0f0c45a1aa73473523d170268b46cb851927337a49eab734d`  
		Last Modified: Mon, 12 Aug 2024 17:02:04 GMT  
		Size: 112.0 MB (111981272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae433ce2ef7950b07b5fb200ef9062f79764bb041f3a3f3f2aae732d84cea576`  
		Last Modified: Mon, 12 Aug 2024 17:02:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc840c164941ed7e908e4c9c106c9f8de39642e63f49aa84fa953d386cf4295f`  
		Last Modified: Mon, 12 Aug 2024 17:02:01 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa7a96408c30b5e950364a89870a69d0694578c35e2f6f06c6c722ae433b95`  
		Last Modified: Mon, 12 Aug 2024 17:02:01 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:7b730c54e040545be92c639f6e567c7c0b00f21e9b766213b551a447e7c56e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6317d792a111d428bb12b5556ec511a75cf7fa0be76d572c666f2aa5229a4a`

```dockerfile
```

-	Layers:
	-	`sha256:bb99b2a0e3d0794d95acd2d2c52e89a95f426bc61740796f336d846f1d46a3db`  
		Last Modified: Mon, 12 Aug 2024 17:02:01 GMT  
		Size: 3.9 MB (3923330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2b3ea4bb15a167da712daec4d57e2f2551cbf68a5e98891856bd12f3c288ae`  
		Last Modified: Mon, 12 Aug 2024 17:02:00 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:1f54d97c8fcdfb39581cfcef3105ccded15c4b9dcb36c0e247c8bb4bb4113878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144414667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc097b9129119fcc38f5683f16b35e883d4014ba2fa072cc05a4b5f50cd171cd`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=11.4.3
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: MARIADB_VERSION=11.4.3
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
	-	`sha256:bff0a3bf8c28b31ae77fd47137ef0644496946afca0cd54db1d5b3a371c271ce`  
		Last Modified: Mon, 12 Aug 2024 17:04:23 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee3ac6a32a1efdd3156d7ca6b54d6452a7fe91ab511942c37fce95bc227534`  
		Last Modified: Mon, 12 Aug 2024 17:04:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d59d1702c710f7e1a4905f93b11a8270c88921487f3217b70fbd3be231e416`  
		Last Modified: Mon, 12 Aug 2024 17:04:25 GMT  
		Size: 106.3 MB (106336097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11ab3b85d231158f9b3e6a02befb7a9d6751bfb7ba9828e48438cae8290bf6e`  
		Last Modified: Mon, 12 Aug 2024 17:04:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842afb0c59e24668189f5ce63e983a0a5bbf6bf099bcb504d3ef5924dae1819`  
		Last Modified: Mon, 12 Aug 2024 17:04:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e047e918a0089cb5c53b592374094867bf8760537f1dd9e3e4763838691e62f`  
		Last Modified: Mon, 12 Aug 2024 17:04:24 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:75a04f58f63ceabd501fe06d03c5c7adb33d49dbf46fcc4d62a8853f47683319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da06297b6801e77f234069ff05f5d72a68d58e4e8649e5ab7743c912cd91061a`

```dockerfile
```

-	Layers:
	-	`sha256:0a72694ee24e6009df84a5937085a5cb314fe5e5527c93473a5e70494257cd3b`  
		Last Modified: Mon, 12 Aug 2024 17:04:24 GMT  
		Size: 3.9 MB (3923303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38907fc983cac3e81aae0d8dffca120089e74e0470eda7d3404e141e18b3a48`  
		Last Modified: Mon, 12 Aug 2024 17:04:23 GMT  
		Size: 30.8 KB (30754 bytes)  
		MIME: application/vnd.in-toto+json
