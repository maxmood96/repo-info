## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:5d08e22b53ae89504133bf61cdff5fb7a8caeb62f1e865cbb00e1f039dace22d
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
$ docker pull mariadb@sha256:7438c099df5114d725a1cb647d475d3144309b3acf6dbe988acab9845c5a5918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167365563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40290ca2e174064e4aaf00193f4f7503441d08b5bb75e4215c5061e56cd0402`
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
# Tue, 20 Jan 2026 19:14:31 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:14:31 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:14:31 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:14:31 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:14:31 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:14:31 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:14:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:14:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:14:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:14:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:14:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:14:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:14:53 GMT
USER mysql
# Tue, 20 Jan 2026 19:14:53 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:14:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e7488440892661aa6ff8b93f2dcf36220a38b4f30282b6fe644dc025ca9723`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca28ed5239b6f582e0999627780c5a62670ae7a15408532390dbf237f24f0656`  
		Last Modified: Tue, 20 Jan 2026 19:15:24 GMT  
		Size: 2.0 MB (2005786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e2694d7542082bdd644ff8d701502b69558ab1e27b98774be0babb087d5e25`  
		Last Modified: Tue, 20 Jan 2026 19:15:27 GMT  
		Size: 7.2 MB (7199641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2bd71cd68464373a39b2882e6013becace6f8b7170a5431022db654dac296a`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4245bd89d8822b1473d8d3096c8ce3d02c9225fc9f8fce3fb71dbf8d02cb6028`  
		Last Modified: Tue, 20 Jan 2026 22:37:30 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea091faa54c90112f2901b3cdd93cabfe742fe4f0c2d8cffba2dbdb37736835f`  
		Last Modified: Tue, 20 Jan 2026 19:15:18 GMT  
		Size: 118.1 MB (118108987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5879d70bb768416ad60c64aecfdf601f29139945580aaae2980f34265f55f4a5`  
		Last Modified: Tue, 20 Jan 2026 19:15:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be29963c611f5c0cafe910d24a5dcedb0844d51f9119f28105558eb5430a7eb`  
		Last Modified: Tue, 20 Jan 2026 22:37:31 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a6e870b6408013953049c7c024196b500efb12fd6df6a912c47f4b7459ccc1`  
		Last Modified: Tue, 20 Jan 2026 19:15:16 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:81ec4ab6a9647f8ce6088bae88b31c2a508c06e591aa0c12c7b62f96e8df42d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41448ecaff79226a2d7f6ea3b9a590e192a7757218e996282fbfa12ad2cdc84`

```dockerfile
```

-	Layers:
	-	`sha256:2a4b2c90fc772af481edca5c9ee530372ac80644961a6286ef4256d757047284`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 4.7 MB (4730599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5552711cc4eb4e04fb16b7ae3198b50170148873c50fcdffabe2efc98672dc4a`  
		Last Modified: Tue, 20 Jan 2026 22:36:37 GMT  
		Size: 34.4 KB (34426 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:045b0b7b11198c92a5f1257b3a0e2662a9e606ba59733b24996dcba87c481b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162687757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a55dedbbc3bd429e747076983b756c9fa6d87138a5ea8f39aa46e2f604c0239`
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
# Tue, 20 Jan 2026 19:15:40 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:15:42 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:15:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:15:45 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:15:45 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:15:45 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:15:45 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:15:45 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:15:45 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:15:45 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:16:13 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:16:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:16:13 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:16:13 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:16:13 GMT
USER mysql
# Tue, 20 Jan 2026 19:16:13 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:16:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e197267862869763ff8d74adc90162408ad79ecdf42caecbb9f68b2088134c47`  
		Last Modified: Tue, 20 Jan 2026 19:16:33 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da14eb17b8d332d71e24bc909564560c0c545158c42b1337d474bad19765e1ef`  
		Last Modified: Tue, 20 Jan 2026 19:16:33 GMT  
		Size: 2.0 MB (2002531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dee967340d3545fbc8ad32d784e22e74b0cf37814c02bffacb9fa2e6e72e39`  
		Last Modified: Tue, 20 Jan 2026 22:37:56 GMT  
		Size: 6.1 MB (6142276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5bf3c00954ebbc9e19d99f776fb4e14abc94c69b5a8ecf11886a784611f8e2`  
		Last Modified: Tue, 20 Jan 2026 21:11:56 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7a7a3e05e352580b883f498e3bedeb26cf862db57e146dde9148d5a7fe17bc`  
		Last Modified: Tue, 20 Jan 2026 19:16:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f19d90c578e39f0585d11d5d2d5b25bcf8008c75e3d9e66c7a884c2301d18`  
		Last Modified: Tue, 20 Jan 2026 22:38:00 GMT  
		Size: 116.3 MB (116316333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580c6eb0185ff40fee822dfe4743ad31ea10ee00bd7b9d468221344d35fa469a`  
		Last Modified: Tue, 20 Jan 2026 19:16:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd443f2cae90748d29891144382d21cd08077f6cfe60e389ab9b6fe426874c39`  
		Last Modified: Tue, 20 Jan 2026 19:16:44 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d520c565b66451fc251046b1b44405befc1b5061d0f7770cd83c0ec413edece`  
		Last Modified: Tue, 20 Jan 2026 19:16:44 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:9d1356455d509cc8ad8592f897e75106ed801bc0a21efebade05c80b41d596f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc1e8bc1e54230239ce9d3fc3f8e07de0123538edd1b699d2294c76ea99c13f`

```dockerfile
```

-	Layers:
	-	`sha256:26b67329cb5ae3014070a45b0ddbfb0175466a136c4d428e2a9900c8ba001e77`  
		Last Modified: Tue, 20 Jan 2026 22:36:40 GMT  
		Size: 4.7 MB (4729434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cba92a11249f0799863266d7c581d40df030a187d78277ccb2e60ed5078a7a1`  
		Last Modified: Tue, 20 Jan 2026 22:36:41 GMT  
		Size: 34.6 KB (34633 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3b53bb5ca815d720d51c3ca5fc1ca0ac5adefad15b5639d49f7d9ff783807b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177554402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd64662cc694e41a17a83b9520f19a5df81a278d1dd13e0a4344fc6100ecb9c`
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
# Tue, 20 Jan 2026 19:18:39 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:18:40 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:18:40 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:18:40 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:18:40 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:18:40 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:19:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:19:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:19:55 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:19:57 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:19:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:19:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:19:59 GMT
USER mysql
# Tue, 20 Jan 2026 19:19:59 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:19:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:36 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17250368781b89b57b5ea27db64dbf8406b736b79eee40482d3ed7bc9fc0985`  
		Last Modified: Tue, 20 Jan 2026 19:26:13 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d836e627067aa0ec36f1f008a9a05c614b66e2019b41a3fbed185c274a23570`  
		Last Modified: Tue, 20 Jan 2026 19:21:16 GMT  
		Size: 2.0 MB (1999801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2696b452c5fed6c2cbf1df9164684017d3b524e0c4fd6f528b41cb847c2ba4`  
		Last Modified: Tue, 20 Jan 2026 19:21:17 GMT  
		Size: 6.1 MB (6143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda8d29429d7b8d2749bd91146ff4394fe40509541cd3356363a2cf06aa5496`  
		Last Modified: Tue, 20 Jan 2026 19:21:16 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a157bc97fa2ff9e4b17f436652817332b3bc4e28a2b64ec15375f2f0621625a`  
		Last Modified: Tue, 20 Jan 2026 19:21:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b96aeb3777c716b52054976ce94e19560e5b93b6adbcfc18f9d4d8d3834d0a`  
		Last Modified: Tue, 20 Jan 2026 19:21:24 GMT  
		Size: 124.9 MB (124933550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84192a629337f6f99e767ebcc2e5698ac189d9aa1232264c58b713397ebba41`  
		Last Modified: Tue, 20 Jan 2026 19:21:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238a1e9f8b8b6bebfa1ba5919a63a3aaf0f7253525651098c349511e4cc1234`  
		Last Modified: Tue, 20 Jan 2026 19:21:07 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a10ba7a611bc8a28e1ddba02663ce47728b5ec7fa9d6d2b83c37432d24f32`  
		Last Modified: Tue, 20 Jan 2026 19:21:08 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:5769f53fd8583efd7d2d9f328f7976e587d09da4f24ded50565323437f4b463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec5233bd361a0675e0cef25fd88d87c06e19e42d82b40d6d41ceb370f181d3a`

```dockerfile
```

-	Layers:
	-	`sha256:233ad3514f9bad0ba0de34919bc895114ff037790a096e8b327cc7afe60c8666`  
		Last Modified: Tue, 20 Jan 2026 22:36:44 GMT  
		Size: 4.7 MB (4724913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95d311a92b86432b5bcf0c49d1f6e893717200aa5e07970a5f5704b2b07cd5`  
		Last Modified: Tue, 20 Jan 2026 22:36:45 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; s390x

```console
$ docker pull mariadb@sha256:79894043e6b8860e55dc44526f2cfffa02e228c8d3321b6a539f2f51ed9cb654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164747663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd7e6a8fb428ccc34f9578f17aa0269e2184a7fe68ef92c5aa004dd7019e41c`
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
# Tue, 20 Jan 2026 19:12:44 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:12:46 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:12:50 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:12:50 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:12:50 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:12:50 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:13:16 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:13:16 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:13:16 GMT
USER mysql
# Tue, 20 Jan 2026 19:13:16 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8d0fd9f50ed7506edfb499eb958eedd9d04f1fe7d6ebb11e4c454c579c856a27`  
		Last Modified: Mon, 19 Jan 2026 06:13:30 GMT  
		Size: 38.1 MB (38120160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de063497ffd42b0e7f4619471776ef4c6a806aa29761a2b199b31763b79444f8`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3a3611a95ec310336ab4e7c31eeba410672474c2d0566b676f26e3dacff31`  
		Last Modified: Tue, 20 Jan 2026 20:05:35 GMT  
		Size: 2.0 MB (2010196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e2f56dba058ddff3aa654e9982e3c21729a786c7bb55e35fab951d7f88791`  
		Last Modified: Tue, 20 Jan 2026 23:08:46 GMT  
		Size: 6.2 MB (6166153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c668bb065083cf2a7a376617097cf3288a689dfab32026439791bd51838193`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d83a218a829b32c418bf596073d1dd7d23c532bbd1d5dfbba7fb2a274732716`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b54216e8e466324d75379c7a1790743825d30e07fe8dac90cd1318ea274a7f`  
		Last Modified: Tue, 20 Jan 2026 19:13:50 GMT  
		Size: 118.4 MB (118433212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be72f14e2eb006c2bcc0ff5682b3668b74d33e29fe1494e920742cadbfab65`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90854e671cd52fead45dd6709469315655b0d3f9cf7731611c953edfa309b900`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d459ba5529bdecf0efd7b8e65283cc0722c7715ebcf833a2175f7beae46714`  
		Last Modified: Tue, 20 Jan 2026 19:13:49 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:a687a3151956a71be2f8478a4fc58b41da465ca417cb6c7bd95ab435f258bc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7534d4a27b839f6cc7d1faf6bebd5221077b31819b71a455282da3a3dc4243ca`

```dockerfile
```

-	Layers:
	-	`sha256:c99fe1d84760c652ba26e6019c91da5246dd83cf328ed4bc183dc4481b8c1155`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 4.7 MB (4719333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887a4b1fa1683f00ad39403318257133de8194b014d7690e8e5d72c765515740`  
		Last Modified: Tue, 20 Jan 2026 22:36:50 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
