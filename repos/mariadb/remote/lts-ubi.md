## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:62246b1d548cd5980bccadcbacc6907ddb1a44144c5b2fb7890db3d19e0e6f44
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

### `mariadb:lts-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:a069a2f5602233c80388ab6cf82fb262b1afbbbdb810a22ee9fb841ae13dbd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145435396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752b87757a3c51f7ea174b1c258fa008662beeaebee8a5285667cc5856e05b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:87021d55df71c4e3f216afb8a8fafe806663072c4406db403bba88d029cd4114 in / 
# Tue, 11 Jun 2024 02:37:24 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 11 Jun 2024 02:37:24 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 11 Jun 2024 02:37:24 GMT
ENV container oci
# Tue, 11 Jun 2024 02:37:24 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -rf /var/log/*
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL release=1194
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:5044c31992c75e94cf041ad1beda86a0b218ead5785a55734e242465ef7798db in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:97862c9bc77fad8fca444d897df1eb9d08bd77f12f61288c39c576743736d49f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 11 Jun 2024 02:37:24 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=11.4.2
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:247c2d03e9487628cb6754ff5385a670df160f7bba36af8fc1f2066e461dc36e`  
		Last Modified: Tue, 23 Jul 2024 23:20:51 GMT  
		Size: 38.9 MB (38868726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a704135ea9bd2809ec23d98bc5c339a06a58c4f8e10bbf3af55fe4d0f1ccf5fd`  
		Last Modified: Wed, 24 Jul 2024 22:59:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86adf7ba4f649cf0751549802b3c5be6c5314ef60e498234d0a709f58111d2df`  
		Last Modified: Wed, 24 Jul 2024 22:59:00 GMT  
		Size: 983.5 KB (983470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eb9591588c0edd67e5229f87e05d8308f5f2347deedd46afdc1338b1b562f6`  
		Last Modified: Wed, 24 Jul 2024 22:58:59 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4c754a80d3f96635e8bd9253e8d54a10ecfbe64bdfda8726acdd095a2ed36`  
		Last Modified: Wed, 24 Jul 2024 22:59:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a3bb472d7ec90e9d10877dd556c2e2a3fc158b9ab6bb15961cd87d6005ee6`  
		Last Modified: Wed, 24 Jul 2024 22:59:02 GMT  
		Size: 105.6 MB (105569538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772c7b1433ee9c87cec8a5bbce9c57768f26af8661046f62365e3f85be6977a0`  
		Last Modified: Wed, 24 Jul 2024 22:59:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ceead9b959c1484152ab771595b3bf3879e773b0245227f9902f00ca43d1b4`  
		Last Modified: Wed, 24 Jul 2024 22:59:01 GMT  
		Size: 3.6 KB (3630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede3f17bed9cc6fdedd29e8d2f4405b0e75a49ada172de15f9d452b90bdceeb6`  
		Last Modified: Wed, 24 Jul 2024 22:59:01 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:a2c23c1a6bccaf199257e78c70d940dabba6976cbeb6681615c88e92811aa448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd400a505b88630b3fc48614fa4bd7cb00bfa4832b8f2af2c7868b6b233506e`

```dockerfile
```

-	Layers:
	-	`sha256:c843998e7366d50f5acea71bb0083308d502008c2cbb24934777bd1a46e4f4d7`  
		Last Modified: Wed, 24 Jul 2024 22:59:00 GMT  
		Size: 3.9 MB (3922167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f56cfdc322dd5ab98da7172b1b68fc7b99ee9040c91f9678d22596c2057d19`  
		Last Modified: Wed, 24 Jul 2024 22:59:00 GMT  
		Size: 30.6 KB (30603 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b6c1769b59856de7aaaca735e3d1c0bf702d254ecbcbbffc0e1c0f6c1875a24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142006472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116ca107b993d95d3fdd04227f6eac02ed8a51a54c122b94865a2a02399557f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=11.4.2
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24451cf0a25948990a22be75714322b70b28f6ab772a4c3c53daeb4cfa8d3e66`  
		Last Modified: Fri, 14 Jun 2024 03:55:52 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717dd27e091e5c77a7f3e48f9c460fb2a15b4f8345aead930156dda527f85bae`  
		Last Modified: Fri, 14 Jun 2024 03:55:52 GMT  
		Size: 913.8 KB (913810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd9bd3b9982620a7250a211b8a6d5a2d01b847d0b8999eac8045c86ba0942ab`  
		Last Modified: Fri, 14 Jun 2024 03:55:52 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a680dc636f5bd6df696dcd191123ceaa630c11fcc8d976c29dc2c90337c2e`  
		Last Modified: Fri, 14 Jun 2024 03:57:04 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f8a3da7e8ece30b4ebc2cd7ad8c1aa93a9e2510af30f9ec9c6c1512b66bbe7`  
		Last Modified: Fri, 14 Jun 2024 03:57:08 GMT  
		Size: 104.0 MB (103960606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0cc36b0335848023ee256a42ea805784a44bd94d828429401993715f7e35f1`  
		Last Modified: Fri, 14 Jun 2024 03:57:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24454bba5b6fef8f0a4c70acb97a0b777d1d065710cbc9bef30d423141e774d`  
		Last Modified: Fri, 14 Jun 2024 03:57:04 GMT  
		Size: 3.6 KB (3631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b97306b8314758cc4a9ed1040b622abcfa6290400eca395fcc188b62e41bb8`  
		Last Modified: Fri, 14 Jun 2024 03:57:05 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:b7393b2e070883256ccde88687b45b03197cd917f2d430feca41484bee974343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29d6e28a7078f69c9c970221133b59c8ed55a8970a824a88151a763ada0727c`

```dockerfile
```

-	Layers:
	-	`sha256:af8002c57679b44b7759528e0b7a780362ea7f78fddd36230ba91f85bb0dadbb`  
		Last Modified: Fri, 14 Jun 2024 03:57:04 GMT  
		Size: 3.9 MB (3884477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8769cd92d5b9b70344d1a45d1d60cd5c4ced24b74cdab1e4a7257f3aa0ab585`  
		Last Modified: Fri, 14 Jun 2024 03:57:04 GMT  
		Size: 31.0 KB (30959 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:fc7127a9f710abed74b606eefb5825053d2d2a37f95c1c4094750c04e69299e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155968117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48494d42ea374186e268cf804340d0c379f6bf0e5b8c00dd79c24ff305ffb627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:47 GMT
ADD file:08e799b553ca381241eb51a31a1ee7c9ca460c662c2c16a91f95cedffe556f65 in / 
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:49 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:49 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:49 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:49 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:51 GMT
ADD file:d5256988023f3e471eb14a7af9564f7c60a67157fde7e15bf77b2e1de43dae53 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:51 GMT
ADD file:46bfa545b2d866eea3fb9f054d54e5e57bbab38aa0340aca4ca393a489cfa2ba in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:52 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=11.4.2
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8b8b86a0ce1c4731395e06bea9200f9baa7149a52efacd1e4802e0e18d2d532b`  
		Last Modified: Thu, 13 Jun 2024 12:10:19 GMT  
		Size: 43.3 MB (43338217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa13316c7ded105c2ef8608a9e640973fd4b9d79153e3511e03e7919f3b30e`  
		Last Modified: Fri, 14 Jun 2024 12:05:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dadf0b67c000154762a26b929a26d22984772c441ae5aa21497dfc07f4f5d3`  
		Last Modified: Fri, 14 Jun 2024 12:05:32 GMT  
		Size: 904.3 KB (904296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa092046b250b77f4cac25f875593996f12f357085a91101cc9c608d269065c`  
		Last Modified: Fri, 14 Jun 2024 12:05:31 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d387d0911c4c895fe5c67efb8fbd2e41069a24184dbb9fe3fbb6af5eedbbd306`  
		Last Modified: Fri, 14 Jun 2024 12:07:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3914eda41bee29e5c21e922988f2ab99a23fc5925297f3118e0a3bdb1e25129`  
		Last Modified: Fri, 14 Jun 2024 12:07:34 GMT  
		Size: 111.7 MB (111711942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf124bbfc0588555dfcddce5222fda345d52d1685969d9e277afe93ed58b22`  
		Last Modified: Fri, 14 Jun 2024 12:07:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e8e2c2250736200441b8fe913968de5a60822b301043c88838cefa3089c283`  
		Last Modified: Fri, 14 Jun 2024 12:07:31 GMT  
		Size: 3.6 KB (3628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7dd6e0586ee6548b7fe09ab0b391861e9acf108a3bae4372cfeed85ff91200`  
		Last Modified: Fri, 14 Jun 2024 12:07:31 GMT  
		Size: 8.4 KB (8376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:95baa78b263f9393ac0ebd1518ae6638354a80cd2e80e65443d6bb7fe5d35013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b7aaa662e175953bf1cc0adea4eb68f3ba8e1e0964a2252cfd40f0e01c7c34`

```dockerfile
```

-	Layers:
	-	`sha256:25054c3933703948011ee8cdf03a10d9b354db1bddd083a4aadcfd9b4ecdf5ef`  
		Last Modified: Fri, 14 Jun 2024 12:07:31 GMT  
		Size: 3.9 MB (3885670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b47407eba3a23dfdeb36bfd4e49a582cd22a0b1c64cf4174b081f16956b12f10`  
		Last Modified: Fri, 14 Jun 2024 12:07:30 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:8dcbe62d0fd6ffc668695ec5cc9a30719fd2cfb909a2220f2f387c56b37e49de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144180213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524cbc3d2fe9cacaa446320c9e7c23c0faad45b9b08090d244396157711d8e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:1a0498fcbd53ea6a4cce5caa1a166c86ab5a3d63fb2e6f1005f6229cd3fd8ddc in / 
# Tue, 11 Jun 2024 02:37:24 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 11 Jun 2024 02:37:24 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 11 Jun 2024 02:37:24 GMT
ENV container oci
# Tue, 11 Jun 2024 02:37:24 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -rf /var/log/*
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL release=1194
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:260b735774b29b332765c57758623137b24eea7dfd0749ddc4f622d177cc9a81 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:6c5a2a1a67a074079cab4ce304a1b74e6ebbcec0d31479580388db97c242c818 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Tue, 11 Jun 2024 02:37:24 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 11 Jun 2024 02:37:24 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=11.4.2
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
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
	-	`sha256:60572e9d2a637984a44ee25d0d9c323f3eca4bc9ad40961543d4fff3b09f5666`  
		Last Modified: Wed, 24 Jul 2024 23:08:21 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c96da890eb100d3d6ffe263d42247899cc7a0674730aa30ece96dcede046ac1`  
		Last Modified: Wed, 24 Jul 2024 23:09:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d00b011ce9ccc2b7de9a38362774fb22cb61d14b9e7a7ee7db0c6d26452ef`  
		Last Modified: Wed, 24 Jul 2024 23:09:37 GMT  
		Size: 106.1 MB (106101915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccac8283438921edbf2343d089a616ae9c41a6a34abb7d5a0d48a64fa98f144`  
		Last Modified: Wed, 24 Jul 2024 23:09:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f796c87660db3c51d3ea9e3117146bee6e1299644f004eb0b3a49d6b52de3853`  
		Last Modified: Wed, 24 Jul 2024 23:09:35 GMT  
		Size: 3.6 KB (3628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a927c2d534eee5ac8c9ccabcf3771a7bd1b43ef5f3ff9e22c08400485833f465`  
		Last Modified: Wed, 24 Jul 2024 23:09:36 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:930ea6108a3ec6148249dd858cebb856311a8053a04ecb9116928b94e23d7644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e69d323c9054275a11daaf95d65bf4dbb258d68f1dfa33862c6ca76c1be446`

```dockerfile
```

-	Layers:
	-	`sha256:a22d8403f5076f6cb497c303cb0e89a5ec534455eea387b07f4d05f132029878`  
		Last Modified: Wed, 24 Jul 2024 23:09:35 GMT  
		Size: 3.9 MB (3923303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca34aa630b304ac2e0648c84a1f43d7daeba12c69e50501305648d51a4cb16f`  
		Last Modified: Wed, 24 Jul 2024 23:09:35 GMT  
		Size: 30.6 KB (30603 bytes)  
		MIME: application/vnd.in-toto+json
