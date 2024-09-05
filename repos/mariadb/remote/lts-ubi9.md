## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:17f9ad0827664f9c07fe1da98c3274abfe400e0eb218af9b14694e379e7f64fd
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

### `mariadb:lts-ubi9` - linux; amd64

```console
$ docker pull mariadb@sha256:10f0feb0f417f8384dbd21773a700f7d9f20ffe14b590919bd0ee663234bf056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146096704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb7517cb37a08ebfcc9582d5b7b4a5fa6230d21b73d94bd7017b7a2eb1a17d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:28a4a75a9aeca0a5843143d1d87f7e6aefda81bdf346196d22398dee9b7df3d3 in / 
# Tue, 27 Aug 2024 14:03:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:12 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:12 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:12 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:12 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:12 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:13 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:0b1fee39b7bed921468ebab3ffc98a2ab087629c37a0e3e3cb03b93101e57ebb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:200862b6d11d841a68f9e14872cdabb79746d525114364781cdd4db91dd45267 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:16 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
USER mysql
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c0ca389759b542396e6b30afcb100a3823d3b343bc847eee7f60d609a106f674`  
		Last Modified: Wed, 04 Sep 2024 07:33:30 GMT  
		Size: 39.2 MB (39158889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a692b7b2bbf67db188311aee4ffb3b96e76cac26d6382c721ac395f0508bdd1d`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420f67a9ead3e2a49f246c5a11b1e0be15eb3faa094f499e26d6fe9f70fad36a`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 983.5 KB (983466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca413c6f0680f7da47d90b0fcc01f78f37051e510b4b70c85180c034134afd92`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3f9fcd5397da509c3c47c44290ef153b3a3e818853e8f19ff4baac1c701f8`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84911c34a53b98998c70d6a02e9ef324a1dd571f90a24f31089c3a2e7663715`  
		Last Modified: Wed, 04 Sep 2024 21:57:37 GMT  
		Size: 105.9 MB (105940293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722c94d675fea8646d04714697a539686488e35dcc989bf1b67a8a6532842e84`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d1404479cc0e2b0013b2af6e92cc9ad83f2c1b1f9156690928d44eea199262`  
		Last Modified: Wed, 04 Sep 2024 21:57:36 GMT  
		Size: 4.0 KB (3978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee5f8acacf235923ce59e183457b79f09135aedb78fddbd44a991ddbb04fc3`  
		Last Modified: Wed, 04 Sep 2024 21:57:36 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:a7224de8d20e06ff02ccb63772ef88f7e636dc28707a9f5147d2d06329ea8458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52801ec1a2d525c22e37a88644df829570e193bef66c53763a8b07040f3e831`

```dockerfile
```

-	Layers:
	-	`sha256:08b11d198bc1b06245f1e16c1cceb47f4abfa7162ccf6bdcd3b45f92460d7987`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 4.0 MB (4024313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb7dd896c720a92617c6375718c3b96e43e0a353a318aaae26357d8a36d3e88`  
		Last Modified: Wed, 04 Sep 2024 21:57:35 GMT  
		Size: 30.2 KB (30151 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a2d1e943900bb52e82e0460b00096f302d10e08158949e4e8b80c2d8d884d3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142474334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e01063c532da16a6af0039c77a7bd191c4174dafa5bd97833fc64f578bd9495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:9a5f39ba1f98c406e15a468dde96a97890537c615e6855d570753065003706c9 in / 
# Tue, 27 Aug 2024 14:03:12 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:13 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:13 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:13 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:34b7dbe1b5044530865977e137b95f472d40aa5287f2d845e436e943ed292fb0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:f2f42168d45968aaf5ad1ce77e9c21e661944f67624f2f1bb4e37bb2da84056a in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
USER mysql
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83e0d15826a8ceb224771cdacee673e782c6608cbaa3de01e33c5d01dc968d1a`  
		Last Modified: Wed, 04 Sep 2024 12:09:37 GMT  
		Size: 37.3 MB (37301947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f97f3ee2dfb83fc6eecd7c9a43e0125a3a711263eabc71ebd96f16fbb8e3ee`  
		Last Modified: Wed, 04 Sep 2024 21:58:48 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85b521d1c09c3af3c41b63c189351d5c8507afc4d961be878b708ec5e8c12`  
		Last Modified: Wed, 04 Sep 2024 21:58:48 GMT  
		Size: 913.8 KB (913806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c2cb504e3d522c5f5e5ca808150b9835590157c740c682364acd24f05ab85`  
		Last Modified: Wed, 04 Sep 2024 22:01:12 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6eae2e29214020a0ec1402b4969b02489f174039e699d54e417cedea615cce`  
		Last Modified: Wed, 04 Sep 2024 22:01:12 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994bb0d73eaf4da0b8bb3384713f3c8a8b24b5452dc1a021e7478bf994f2899`  
		Last Modified: Wed, 04 Sep 2024 22:01:15 GMT  
		Size: 104.2 MB (104244526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaa49b1080af14a008f929df5fb07daf6d8117d3215ebd9af75da71488a7c61`  
		Last Modified: Wed, 04 Sep 2024 22:01:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aba2c7a4d73d9cd39efadc6aa85f8988e894eb1dcde99c7e6fede9c4fc2522c`  
		Last Modified: Wed, 04 Sep 2024 22:01:13 GMT  
		Size: 4.0 KB (3979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda45c56ad59096ef2da2b1a0074fe67ab3d2bcb92fe7dae98393b27111c9b0a`  
		Last Modified: Wed, 04 Sep 2024 22:01:13 GMT  
		Size: 8.4 KB (8428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:99213b71a83c1fdcde0b493d59c788c7d0a183d9c0a00daa55a0f88da9279eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3beba09cc83263d74b4bc3578cb35f08a5e1aaba4c503b88c15bb41a076cb7`

```dockerfile
```

-	Layers:
	-	`sha256:1d3e713e3297d54dbb8d094b765dffae73fbb5eb281fb9138620242cad0af0c6`  
		Last Modified: Wed, 04 Sep 2024 22:01:12 GMT  
		Size: 4.0 MB (4024259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d59cc4542b156aca52f67e7d3269367f798280c138b164e6bcac607220f959a`  
		Last Modified: Wed, 04 Sep 2024 22:01:12 GMT  
		Size: 30.5 KB (30483 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6cd181e91f5db199b6de0fd2239cc4fb91652686d32c4bdbd7bf578f0b923934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156553102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496f6b17c6d572f91f225b6063ad59d7b760ebcb52f1bd31b760fae4583d8bf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:12 GMT
ADD file:f007a60e32e08d43c550a97c16f972f39506988b7e247bd6627599e91c17323f in / 
# Tue, 27 Aug 2024 14:03:14 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:14 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:14 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:14 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:15 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:16 GMT
ADD file:a5f8a4fe76e7d622a09fcbcca3627d47677c86bd786397d064531d01811fcdb0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:16 GMT
ADD file:a3679a8847d919079839b3a73f96cc68368baad49ccd60dcbe5305759aba49b8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:16 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:17 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:21 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
USER mysql
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5591fa6d9bf998094d14bbf292637dc73858269f63d69d897a1a64df35d25765`  
		Last Modified: Wed, 04 Sep 2024 12:09:42 GMT  
		Size: 43.6 MB (43628240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803cf9c90190a097ff1c983381a90c6aeb989a44e4da65fee294b7ec8ef3f6b`  
		Last Modified: Wed, 04 Sep 2024 21:59:49 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415fad253c59e6dc7a54026520f53411db52ad33096840133df3cada42903bf7`  
		Last Modified: Wed, 04 Sep 2024 21:59:49 GMT  
		Size: 904.3 KB (904312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f28c0ce4b55c308d4786c57bd45fb024e416ef7db7ffa8abe0d0ca51b040e9`  
		Last Modified: Wed, 04 Sep 2024 22:04:28 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88a6e2af8ba5c90f9d003e1f010745fe13c0de587a71843d7347737adf5a0b`  
		Last Modified: Wed, 04 Sep 2024 22:04:28 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0229c1b05c8c112aafc9bd08060306039f6c990f8f43ee4f2c6f269c143e25`  
		Last Modified: Wed, 04 Sep 2024 22:04:33 GMT  
		Size: 112.0 MB (112006492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bb0a0dd910683d1fed0fb94e371c0923777f475436721ab1880e8acb28f2a`  
		Last Modified: Wed, 04 Sep 2024 22:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8782404717ae682826eed3d8f28ad4405e97bcb0fb15e62d50e3e34697525dc`  
		Last Modified: Wed, 04 Sep 2024 22:04:29 GMT  
		Size: 4.0 KB (3978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d148d2b0ebbb534134c1cc41d33357295d253150bdf643e401d4d4f912c22f65`  
		Last Modified: Wed, 04 Sep 2024 22:04:29 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:02a30dd17c7970c0d20c4e938143244801bd13b6960087a36ddac98a7a469abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e861c49aca53178f0cdd9a22919b90e0a4863ebb2e112cf26dc551de3b17e03f`

```dockerfile
```

-	Layers:
	-	`sha256:cfda43b5062d7ae40c523def41bc9c2faa2e55fb492e9dd45da52222642d7f23`  
		Last Modified: Wed, 04 Sep 2024 22:04:28 GMT  
		Size: 4.0 MB (4025464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cd0720c34aa1aa4ad5520b1b5bca2972ac94f0c2cea74b6b0727162125a428`  
		Last Modified: Wed, 04 Sep 2024 22:04:28 GMT  
		Size: 30.2 KB (30208 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; s390x

```console
$ docker pull mariadb@sha256:1c134b52f0ef48dbe269302c12f17051e898fefc471f5bd0db6ae31712447412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144720625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4174876393cafe70e4e0f33c91d1c92fbcd35d59b56e51fd9e5e54e1bbbe8d4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:3be9883ece0ff5165cc24f0c588e3b42dc016404a82d559b5b886dd6a5b2dd6b in / 
# Tue, 27 Aug 2024 14:03:12 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:12 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:13 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:13 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:13 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:0be936f502a287e8906580e1bf6c9e7ab2575d33a1f300d26347c5ede4e5741c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:09261f6eece8b1a99ffeb75f49833c204551e89b3ba163ce849889c560d99a24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:16 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=11.4.3
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: MARIADB_VERSION=11.4.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
USER mysql
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:fb313ca4b0a99db95fc46c5cc693c9716554d0679ba03a2afd9303df30894b6a`  
		Last Modified: Wed, 04 Sep 2024 12:09:47 GMT  
		Size: 37.4 MB (37402801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5de80e465f741ae9b73eba8903f16aa1576815917ed5d5db3e668e8cec3b81`  
		Last Modified: Wed, 04 Sep 2024 21:59:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac7dbd2f79327e048dcb4e82a911984636f16daefdb75b45b7e662a7256cee`  
		Last Modified: Wed, 04 Sep 2024 21:59:10 GMT  
		Size: 948.1 KB (948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a955d24eee156a63de5a3ee86607a43f0a47eaabeea5ac2aabf99c7f653db5`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8bf23287fce38ec5cde16c73891fc193fea67cc1c64310e683fd986bf183f7`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5210e17b07172a3000aeee84ce2b6c14358dbf62291670f5101301d7d8c045a`  
		Last Modified: Wed, 04 Sep 2024 22:02:06 GMT  
		Size: 106.4 MB (106355640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939916be3b184c19ce4391065e491899d5a5123c21157c5a416f393373c2c389`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62024e60980bfc811e27ee7632cde6b8efc20dc75c1f3955bea0a3a1a2a26b7f`  
		Last Modified: Wed, 04 Sep 2024 22:02:05 GMT  
		Size: 4.0 KB (3979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48e284cfe1cdefa7c5cad52f7ec989d823de4acd63aa5fba0e5ddf2c3894b8`  
		Last Modified: Wed, 04 Sep 2024 22:02:05 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:6500990f3b26289e5233f29226a75478bfb9af248732e750470650657cf647af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4ed7e76acfce13bbd5eee9128fd93ca2566bc5a72de87d2eeb47eca6098621`

```dockerfile
```

-	Layers:
	-	`sha256:c9b1b66eea8c50d6df0aace2ac2748a2438bf6a6af803959c342584f63b49f8b`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 4.0 MB (4025449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aecc21bc908988f36e027f594227f8568ca93f950ddfb5ce74e167a51059dd`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 30.2 KB (30151 bytes)  
		MIME: application/vnd.in-toto+json
