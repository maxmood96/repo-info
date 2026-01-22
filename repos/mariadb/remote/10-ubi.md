## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:2a5bc3f811fabf9563f18daac688ad050f12cf5b6e91b850a087188bceb2b723
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
$ docker pull mariadb@sha256:03996cdfd5ae68e48b16136221f9d3e400d1e9268d498ae72caf4998119e68a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166282922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4188e42a891988916d483fb86962da37ec1d8f4220890b37e8367d6fd8db0f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:14:27 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:14:28 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:14:31 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:16:01 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:16:01 GMT
ARG MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:16:01 GMT
ENV MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:16:27 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:16:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:16:27 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:16:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:16:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:16:27 GMT
USER mysql
# Tue, 20 Jan 2026 19:16:27 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:16:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:34 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e7488440892661aa6ff8b93f2dcf36220a38b4f30282b6fe644dc025ca9723`  
		Last Modified: Tue, 20 Jan 2026 19:15:24 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca28ed5239b6f582e0999627780c5a62670ae7a15408532390dbf237f24f0656`  
		Last Modified: Tue, 20 Jan 2026 19:15:24 GMT  
		Size: 2.0 MB (2005786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e2694d7542082bdd644ff8d701502b69558ab1e27b98774be0babb087d5e25`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 7.2 MB (7199641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a58c1444c2d417583ef10460da8b17557098a82fcaa500051ef883059f7732`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eefc03abaf6fd033254f51a3e7f3d0ef39454d242de91e8f4ca00e8c0ae9e5e`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f028b3aff6ab723fec02a1fedd8de7b1d9c97bcf977efcd091640b51d2fc2345`  
		Last Modified: Tue, 20 Jan 2026 22:35:44 GMT  
		Size: 117.0 MB (117026361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ed482bf1c3182dc25ad89979be048bdebe996a2a199fd46e9f5a5d36d60153`  
		Last Modified: Tue, 20 Jan 2026 22:35:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85451fb501bf3496be528b8f0433d46859f2021427eff1521ceecf0aa1ba74d`  
		Last Modified: Tue, 20 Jan 2026 19:16:48 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c626baba72def7f8e76c12b28ffe7ee657550be43a3698f1719b3f049e492a6`  
		Last Modified: Tue, 20 Jan 2026 19:16:48 GMT  
		Size: 8.4 KB (8363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:b4ed724339dd68b0411c9ac110de5328976a20b655f3dbb1168e0fc0fee43064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48693e07dc77ea01d7a06b7af7d77c1f4599c7686238ce947a6da0699bde1e62`

```dockerfile
```

-	Layers:
	-	`sha256:9bd324d40a681ed8536b2911c936ea8e5a9b688c46a3b77b3afbe2cea6b01451`  
		Last Modified: Tue, 20 Jan 2026 22:35:34 GMT  
		Size: 4.7 MB (4725257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c407b049f0dac6cd4f4e8f34858f36c69a3fb745aefd5892b0d03b3dc33fc5`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:489bcae2548fe5cc98e9d44940fc4eba8f05b19665dd50e8b88a15252fc57f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161552687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52caa5af2c37e0ef9dee1af8b6602c1b299f4f8a99c927a1f54dea463e553c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:16:13 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:16:14 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:16:17 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:16:17 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:16:17 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:16:17 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:16:17 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:16:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:16:17 GMT
ARG MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:16:17 GMT
ENV MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:16:43 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:16:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:16:43 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:16:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:16:43 GMT
USER mysql
# Tue, 20 Jan 2026 19:16:43 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:16:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64813d1ae462fa7184a6f750bf718574e2f9dd548ba2742d4eddb0e2dea02f85`  
		Last Modified: Tue, 20 Jan 2026 19:17:13 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2260d37291709c4b5d733f909fa0876f084fb00e98bc1d2a153e16291a4408`  
		Last Modified: Tue, 20 Jan 2026 19:17:14 GMT  
		Size: 2.0 MB (2002537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b121b1e214ac8eca85646bd5a8560517d1f6d63c07149781c651f9ad4909e2`  
		Last Modified: Tue, 20 Jan 2026 19:22:03 GMT  
		Size: 6.1 MB (6142269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e185875bb5a35f61f478bd6a72cf9e44b02b9414f5fd789a8b7f4afc3be59342`  
		Last Modified: Tue, 20 Jan 2026 19:17:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1617508d25948872d4076fb9d9c8260d7d4d0531986409bbe50e1a86d5f3c`  
		Last Modified: Tue, 20 Jan 2026 19:17:14 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ab8f5351abae200c05e94222bdf35ebec5b65bf60b15d24675f8482300fc0`  
		Last Modified: Tue, 20 Jan 2026 19:17:26 GMT  
		Size: 115.2 MB (115181278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fc49d426e57ec84d64eec24fea1181405391af7c4a9e578c2e26837e6ed89f`  
		Last Modified: Tue, 20 Jan 2026 19:17:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e156c76a4a80b17afdbd295dd4955ce489e0a71fe31b63d558efb17cf4013245`  
		Last Modified: Tue, 20 Jan 2026 19:17:06 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857d430023843313fff97b6be6149187d34f50b1f2471402fc7e3268fc884e6`  
		Last Modified: Tue, 20 Jan 2026 19:17:20 GMT  
		Size: 8.4 KB (8360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:f451a828d7bf6645e521c30f6a6046ed1642daea2ed0d43b78994a723bceb2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efbb0b943ae97739eca6f3be271acbc979513c97e1eccf37de3946c6d61e1cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e615bb33c13d65ae47294690ea551467c1562bd9f00cd1ee1e3e1409434a9f2`  
		Last Modified: Tue, 20 Jan 2026 19:17:04 GMT  
		Size: 4.7 MB (4724068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba46c39a2e241c555425ed571ec152cbbc1f23af2cd6608285b03504766b2c22`  
		Last Modified: Tue, 20 Jan 2026 19:17:04 GMT  
		Size: 34.0 KB (34030 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:62e183d8abd2a57fae4e3cf73564aea4d45eb3ef8b6ea9e64997c40fd17e0028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176253209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e28061dea30602c2a0018463490f69e2a99e0e7b2e209b337e4039a6d9956b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:18:27 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:18:31 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:18:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:18:38 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:21:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:21:25 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:21:25 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:21:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:21:25 GMT
ARG MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:21:25 GMT
ENV MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:22:40 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:22:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:22:41 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:22:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:22:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:22:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:22:44 GMT
USER mysql
# Tue, 20 Jan 2026 19:22:44 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:22:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:44 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17250368781b89b57b5ea27db64dbf8406b736b79eee40482d3ed7bc9fc0985`  
		Last Modified: Tue, 20 Jan 2026 19:26:13 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d836e627067aa0ec36f1f008a9a05c614b66e2019b41a3fbed185c274a23570`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 2.0 MB (1999801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2696b452c5fed6c2cbf1df9164684017d3b524e0c4fd6f528b41cb847c2ba4`  
		Last Modified: Tue, 20 Jan 2026 19:21:17 GMT  
		Size: 6.1 MB (6143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65f832c2f3751c48ca58941f9199a389dbeaeac033608bf2149df9d06b4926`  
		Last Modified: Tue, 20 Jan 2026 19:23:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc086c6a28d90a7b079b434b8e5f75bea776972991ecd0bc1a8075439e19510b`  
		Last Modified: Tue, 20 Jan 2026 19:23:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c52753fd307266cee5f5e4b00711ac120793f37a539f3a12b6cab049ca51808`  
		Last Modified: Tue, 20 Jan 2026 19:23:50 GMT  
		Size: 123.6 MB (123632367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f813a298946ef35120c9fea1213fa4af04bc814125be6e45a89cb7ecf04fa1de`  
		Last Modified: Tue, 20 Jan 2026 23:06:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ab3c52e7983eba09644c2e31f385d018e73a5202c3ef550fa6fed7d3a9f1c1`  
		Last Modified: Tue, 20 Jan 2026 19:23:46 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7574e0073bed667253812d497acc143f1ba98ff90a2de96c21162e00be3896`  
		Last Modified: Tue, 20 Jan 2026 21:23:06 GMT  
		Size: 8.4 KB (8361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:48bb80893a77e72e384511b5aec33ff7c1f5cedf4f67d0b6e5a3ebc72a2ba242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5927558d5eb59f69b292357f5d92419770c66020e955edfa5334845f77f2013`

```dockerfile
```

-	Layers:
	-	`sha256:8dea011b33943449a7d7ca9dfe8e78e46b2c72fc802004c58b181bf104eaaba1`  
		Last Modified: Tue, 20 Jan 2026 19:23:46 GMT  
		Size: 4.7 MB (4719559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0caa1b5daff8a6b2f937b6130d5ad156a804541feb7fb1c1b163ae05676e864`  
		Last Modified: Tue, 20 Jan 2026 22:35:46 GMT  
		Size: 33.9 KB (33906 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:3492c8944af93c634332776080dc8ff3c3bbf6cb59df06a6ed5910c2558f2001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163519851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6a78a81cce40549e441a767e91782a590b0ea9c59eca1ef8bb85e632f2968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:57:08 GMT
ENV container oci
# Mon, 19 Jan 2026 00:57:08 GMT
COPY dir:60e8b920663668133ad1c0beb8ddee0ed0404da0ad2cb12d0bdf023f3692297c in /      
# Mon, 19 Jan 2026 00:57:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:57:08 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:09Z" "org.opencontainers.image.created"="2026-01-19T00:56:09Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:09Z
# Tue, 20 Jan 2026 19:12:46 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:12:48 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:12:51 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:13:35 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:13:35 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:13:35 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:13:35 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:13:35 GMT
ARG MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:13:35 GMT
ENV MARIADB_VERSION=10.11.15
# Tue, 20 Jan 2026 19:13:58 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:13:58 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:13:58 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:13:58 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:13:58 GMT
USER mysql
# Tue, 20 Jan 2026 19:13:58 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:13:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8d0fd9f50ed7506edfb499eb958eedd9d04f1fe7d6ebb11e4c454c579c856a27`  
		Last Modified: Mon, 19 Jan 2026 06:13:30 GMT  
		Size: 38.1 MB (38120160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb12c0b37d9a799d46b219d9987c9ad8af9481e82486a327e9e940eae41c8fc`  
		Last Modified: Tue, 20 Jan 2026 19:13:49 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed9f90927d06cb98caa90fefb7ff635a5211e91174bdae31a9dea8166300f3`  
		Last Modified: Tue, 20 Jan 2026 21:10:12 GMT  
		Size: 2.0 MB (2010186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd45f17fbcc03ff57158a0814e0acd6e6c122dce92b03723bb3cb8bd7d3f72a7`  
		Last Modified: Tue, 20 Jan 2026 23:10:35 GMT  
		Size: 6.2 MB (6166182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12dcc16c3c897b21cb66b2b1aade4b9b2176eaeb43c07b575f7b72d2c8cd08a`  
		Last Modified: Tue, 20 Jan 2026 19:14:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb961cfc925c5e03fa52c00a0725842e779cf80d76a95b632844d5924474ede`  
		Last Modified: Tue, 20 Jan 2026 21:10:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209db79fa2b6e3e6447d379ed606a1033d4012bdc2b9ec29d5aa28510e6918cf`  
		Last Modified: Tue, 20 Jan 2026 19:15:00 GMT  
		Size: 117.2 MB (117205411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b1fe2c8348dcd7a1797e8d3ebce8274fd61984068b4b638efcf61bcc5e66e`  
		Last Modified: Tue, 20 Jan 2026 19:14:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60765b17936ab2bf58fbaaa3b5ab9f9aa0bad96c92503262330c840a0eacb29`  
		Last Modified: Tue, 20 Jan 2026 19:14:30 GMT  
		Size: 4.0 KB (4012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3b68a08c74d8a82d2c0211f200779139452be5dd89de17e91ed3f7732449a`  
		Last Modified: Tue, 20 Jan 2026 23:06:53 GMT  
		Size: 8.4 KB (8354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:a3b19dda8e4eae403020c8db5c2280901e8c7f442dd708ff98d0545cf52fc533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4747838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a97370fc5bb6da85fc82b969edcd6d8de8c984f0f3a2c6ad0cac12c6f24e9`

```dockerfile
```

-	Layers:
	-	`sha256:20e2ff7aa820db6c0766d9657f94aa29c962895d7eb1a7101d75216bad939cc4`  
		Last Modified: Tue, 20 Jan 2026 22:35:49 GMT  
		Size: 4.7 MB (4713991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccff993a60b3c0b602e23d121fd12551e3d46b7aefdc0738691b031f788da01b`  
		Last Modified: Tue, 20 Jan 2026 19:14:28 GMT  
		Size: 33.8 KB (33847 bytes)  
		MIME: application/vnd.in-toto+json
