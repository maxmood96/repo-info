## `neo4j:5-community-ubi10`

```console
$ docker pull neo4j@sha256:7c0537583a2f9a06a1361f7e96fb29ca6146ba36f060d40c878156e017d9b55f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:02a5b64eea1fddedf58ea35be843fc49611772a220c0dff9b06a5ac14ce72148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287392653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210aeedac6b4d32692a907636b5f1bed96c8f2edf607b510c5b693b399b4790`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:20:48 GMT
ENV container oci
# Thu, 26 Mar 2026 17:20:48 GMT
COPY dir:013378efc21240669710b39853c72e001fd6ffb5e0383845178fe8e7ffe47e8f in /      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:20:48 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:20:31Z" "org.opencontainers.image.created"="2026-03-26T17:20:31Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:20:31Z
# Tue, 31 Mar 2026 17:48:10 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 31 Mar 2026 17:48:10 GMT
ENV NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 31 Mar 2026 17:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 31 Mar 2026 17:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 31 Mar 2026 17:48:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 31 Mar 2026 17:48:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2026 17:48:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Mar 2026 17:48:14 GMT
VOLUME [/data /logs]
# Tue, 31 Mar 2026 17:48:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 31 Mar 2026 17:48:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:48:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e6c23a286985c06cc6d9b05d3d1e515a2fe5443b2da741ed6bc423f7907d3e67`  
		Last Modified: Thu, 26 Mar 2026 18:05:52 GMT  
		Size: 34.6 MB (34608408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d43e4b826da1865c69e1949408369c10974ac56170c97fd6d4b90183b47e86`  
		Last Modified: Tue, 31 Mar 2026 17:48:34 GMT  
		Size: 85.9 MB (85867645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bf5a1abeecbca7de24f1a01624393f4539bb1758c38cb6630c1e33b7db398c`  
		Last Modified: Tue, 31 Mar 2026 17:48:30 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617caf44b70a99c8f9e1ce62b236925059ff004d78e8c3b13de85f6c4361372e`  
		Last Modified: Tue, 31 Mar 2026 17:48:35 GMT  
		Size: 166.9 MB (166906510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:b265cc633e05d675244a38ccb86f3853698dab3885b5ade97fa49c7ac7951f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1632469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c897e6d9a8ed562601b601d36d320943434be78de37f40d0ef0b1bc407b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:caf38c760f11a0dce8624405717d9d8f8bd708f890996d31ad758f192f9c7764`  
		Last Modified: Tue, 31 Mar 2026 17:48:30 GMT  
		Size: 1.6 MB (1611520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5561d2a85e714d622e3e5c8836e53976b924d5ecf51ea4e9dd81029fe1f305`  
		Last Modified: Tue, 31 Mar 2026 17:48:30 GMT  
		Size: 20.9 KB (20949 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a419c3b97211f97d0d1777e69e894563e53080aff0be9722b2bdab295b553a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284400214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaee7108f3e644bfa36e26232d2f2b2c523c1da5d9da2c6c3c4459abf0878dab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:23:52 GMT
ENV container oci
# Thu, 26 Mar 2026 17:23:53 GMT
COPY dir:7d6c6936964da50429cf71ef4747883349075c5f65fea997c68d435e4becb027 in /      
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:23:53 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:23:36Z" "org.opencontainers.image.created"="2026-03-26T17:23:36Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:23:36Z
# Tue, 31 Mar 2026 17:48:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 31 Mar 2026 17:48:04 GMT
ENV NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 31 Mar 2026 17:48:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 31 Mar 2026 17:48:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 31 Mar 2026 17:48:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 31 Mar 2026 17:48:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2026 17:48:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Mar 2026 17:48:07 GMT
VOLUME [/data /logs]
# Tue, 31 Mar 2026 17:48:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 31 Mar 2026 17:48:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:48:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3bdc97aa816d30cff74675555d7b3f29b652ed3811ef43aff9bf264de81602f2`  
		Last Modified: Thu, 26 Mar 2026 18:05:46 GMT  
		Size: 32.7 MB (32681363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057435b4d6a44dcc58ef4e8ec72e837173545a00fa505f1e72a8598981b2caab`  
		Last Modified: Tue, 31 Mar 2026 17:48:27 GMT  
		Size: 84.8 MB (84802191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a875e2c8f75633d548f1605b856c6ef3434314864fcf2e4ebf7d2d3f276b70`  
		Last Modified: Tue, 31 Mar 2026 17:48:23 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cc670419d201aa6173548d2580235e39763f7c6f7acc5a798326344fe9653`  
		Last Modified: Tue, 31 Mar 2026 17:48:29 GMT  
		Size: 166.9 MB (166906568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6b9c69fa2ab5255ea37ba4033e5fd256be7c4acb1f1d171e4d81dc1d14fb9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1631889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a45ba1fde871571bda2e97251fce6d679a5a170dc5d03b1f9b7bdc34f8f122d`

```dockerfile
```

-	Layers:
	-	`sha256:73e7018642ae0bc5c48b70a61552d3ce1ac4767d69c4383bc3909135b7f9d615`  
		Last Modified: Tue, 31 Mar 2026 17:48:24 GMT  
		Size: 1.6 MB (1610803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7bb4eeeaa53ef0e44c6a4eed17d85f61df062201c4edf4a07c8fee3fadda55`  
		Last Modified: Tue, 31 Mar 2026 17:48:23 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json
