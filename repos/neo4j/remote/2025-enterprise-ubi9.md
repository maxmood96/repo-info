## `neo4j:2025-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:641f868eb141d39fc91ea1e03cf04192b443c30ec423f690609e859fd3a88371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:b71aa60269e50972f79465b7115ba9e562fe926f89a2f0f7158e52fcfbc33a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504808707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77e06c3457df99194819a36461f9573c89e02c040a9cd73e645e943dd93c007`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 27 Aug 2025 14:31:02 GMT
ENV container oci
# Wed, 27 Aug 2025 14:31:02 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Wed, 27 Aug 2025 14:31:02 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV NEO4J_SHA256=6818a98fca5044976e23935e9fc415aa080c9f36d4546274f7a8486cb8096d3c NEO4J_TARBALL=neo4j-enterprise-2025.08.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829587f4d939815afb9d4f1918fcd4b7eadd20cb0abf03a5474509f900f80ab8`  
		Last Modified: Sat, 20 Sep 2025 00:27:35 GMT  
		Size: 131.3 MB (131301003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213d897c01385cf1f7cd7c1adbbe316903a33fc3067a4d24870ff1d9a8867af0`  
		Last Modified: Fri, 19 Sep 2025 20:47:13 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca397e14e56ba0fb69eb49b93b7aa9aa2b985e41470e87632c6d51a7ec056903`  
		Last Modified: Sat, 20 Sep 2025 00:27:49 GMT  
		Size: 333.8 MB (333849402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:096d5706c1ec36dec61ca7e6d37493968319415bcb1925649471ef231ffb6a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5626839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d4cfc3a985f506ae32556a8a097e615b71b99b2e0e85a306145d81133a7366`

```dockerfile
```

-	Layers:
	-	`sha256:4b89415c92cb5d521559893c1966b9292e057bcfa2b5c93242ced3885704ce5d`  
		Last Modified: Fri, 19 Sep 2025 23:43:31 GMT  
		Size: 5.6 MB (5606209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617e5668de2d0c314c0cbba0a5f3411d7ba065de03047a76eec368b6e473bc90`  
		Last Modified: Fri, 19 Sep 2025 23:43:32 GMT  
		Size: 20.6 KB (20630 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:75eb82059f2e6f67bf111755a56fc01d2cf8f454dab1f786c6344c47a991f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.7 MB (502686171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b551cd94e87569acaecd62074c423e12c179720d412fbe1bc7f7903c7dc9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 27 Aug 2025 14:31:02 GMT
ENV container oci
# Wed, 27 Aug 2025 14:31:02 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 27 Aug 2025 14:31:02 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Wed, 27 Aug 2025 14:31:02 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Wed, 27 Aug 2025 14:31:02 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV NEO4J_SHA256=6818a98fca5044976e23935e9fc415aa080c9f36d4546274f7a8486cb8096d3c NEO4J_TARBALL=neo4j-enterprise-2025.08.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0380275874574cc3062fa1f3aadfd6d209d1e3ba4d61f3ee2c3db771de7a2eb4`  
		Last Modified: Fri, 19 Sep 2025 20:46:55 GMT  
		Size: 130.9 MB (130926512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a5f6dc60e388a4680407a353f7e1d949c5f9014dca748e3d8af23893bd1ffb`  
		Last Modified: Fri, 19 Sep 2025 20:47:10 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bb4554f24a3f06f5fe9f799a30019fd276f9c11f055fd969e9db22ae476d54`  
		Last Modified: Fri, 19 Sep 2025 20:46:58 GMT  
		Size: 333.8 MB (333849462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3941797362dd23687bdabb5d54ed32e0d6320f0e3609d1bd9c779d7ff4f7d232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482f90ed3634e189c7c744f9c9f8a0cd3def44658b701941b6e82f2e34153ef3`

```dockerfile
```

-	Layers:
	-	`sha256:dd6e5d49690f2f3b672ea6b4134ba1004bb3c471e048c54cd344a78075c3f487`  
		Last Modified: Fri, 19 Sep 2025 23:43:37 GMT  
		Size: 5.6 MB (5585953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c3099acfcbadd424ea0b31c320d90397fd8746cd7e5b553d510527b761974d`  
		Last Modified: Fri, 19 Sep 2025 23:43:37 GMT  
		Size: 20.7 KB (20743 bytes)  
		MIME: application/vnd.in-toto+json
