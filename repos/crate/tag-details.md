<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:3.3`](#crate33)
-	[`crate:3.3.5`](#crate335)
-	[`crate:4.0`](#crate40)
-	[`crate:4.0.12`](#crate4012)
-	[`crate:4.1`](#crate41)
-	[`crate:4.1.1`](#crate411)
-	[`crate:latest`](#cratelatest)

## `crate:3.3`

```console
$ docker pull crate@sha256:1220d3a66ba7434b40edd63308e7ebb931f7d20dfc03a7f40f24846525d96261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `crate:3.3` - linux; amd64

```console
$ docker pull crate@sha256:28029e531f7aceb85666b0bd67a5d3c1fe45f4467e3ac14bf98e617018a23ce2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344428347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e96aeb3894ea7c822a0142a9fab1a1d0dffe6efa890ef860e56d50476f0adf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 12 Nov 2019 02:27:48 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Tue, 12 Nov 2019 02:27:49 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Tue, 12 Nov 2019 02:27:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Tue, 12 Nov 2019 02:28:47 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 12 Nov 2019 02:28:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 12 Nov 2019 02:28:47 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 12 Nov 2019 02:28:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 12 Nov 2019 02:28:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 02:28:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 12 Nov 2019 02:28:50 GMT
RUN mkdir -p /data/data /data/log
# Tue, 12 Nov 2019 02:28:50 GMT
VOLUME [/data]
# Tue, 12 Nov 2019 02:28:50 GMT
WORKDIR /data
# Tue, 12 Nov 2019 02:28:50 GMT
EXPOSE 4200 4300 5432
# Tue, 12 Nov 2019 02:28:51 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 12 Nov 2019 02:28:51 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 12 Nov 2019 02:28:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2019-07-08T14:08:18.187344 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Tue, 12 Nov 2019 02:28:51 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 12 Nov 2019 02:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:28:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8f68504ec2c5765db548cc2ddcb32937b1072af2e37e1ba56c9e867adc9bb3`  
		Last Modified: Tue, 12 Nov 2019 02:31:20 GMT  
		Size: 188.1 MB (188101325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ad843ad2701b18cddae3f025111abfe91edc8b78735988cfdc7759a30edd9`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ffb4e6dc1ab19b4589ff57e77221320783bce3f50cf263975446e9b166a775`  
		Last Modified: Tue, 12 Nov 2019 02:31:12 GMT  
		Size: 79.2 MB (79246730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e48d3344e9f6d20d253cc9b8c0e62020a424d8d5c1405ea4066f688b01f110`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2105112ea016388d5b835aa32be8f5dfba2e84a40dff93803043b5fcff806`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df92165a3a99469b9cfa588d35c040aa8b7bc8e114422d38cd501397a93563f`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 1.3 MB (1294045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5bbfb4acf75aa2021bd49d72b641da8541333fdd2b67ec378cc391a7aee815`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c192e02a2b87f83721595e911d909829d9aaca448c37c17403a9b63b6a2abc8a`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe1f645884d2346dcef4fe9aaa190fc5ad5614bd3313a541039cd99aaf31b30`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded610082ee63d998ec7c77cb724405d7a42b6c42a5c42f8d824c1a23b279384`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:3.3.5`

```console
$ docker pull crate@sha256:1220d3a66ba7434b40edd63308e7ebb931f7d20dfc03a7f40f24846525d96261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `crate:3.3.5` - linux; amd64

```console
$ docker pull crate@sha256:28029e531f7aceb85666b0bd67a5d3c1fe45f4467e3ac14bf98e617018a23ce2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344428347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e96aeb3894ea7c822a0142a9fab1a1d0dffe6efa890ef860e56d50476f0adf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 12 Nov 2019 02:27:48 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Tue, 12 Nov 2019 02:27:49 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Tue, 12 Nov 2019 02:27:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Tue, 12 Nov 2019 02:28:47 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 12 Nov 2019 02:28:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 12 Nov 2019 02:28:47 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 12 Nov 2019 02:28:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 12 Nov 2019 02:28:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 02:28:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 12 Nov 2019 02:28:50 GMT
RUN mkdir -p /data/data /data/log
# Tue, 12 Nov 2019 02:28:50 GMT
VOLUME [/data]
# Tue, 12 Nov 2019 02:28:50 GMT
WORKDIR /data
# Tue, 12 Nov 2019 02:28:50 GMT
EXPOSE 4200 4300 5432
# Tue, 12 Nov 2019 02:28:51 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 12 Nov 2019 02:28:51 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 12 Nov 2019 02:28:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2019-07-08T14:08:18.187344 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Tue, 12 Nov 2019 02:28:51 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 12 Nov 2019 02:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:28:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8f68504ec2c5765db548cc2ddcb32937b1072af2e37e1ba56c9e867adc9bb3`  
		Last Modified: Tue, 12 Nov 2019 02:31:20 GMT  
		Size: 188.1 MB (188101325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ad843ad2701b18cddae3f025111abfe91edc8b78735988cfdc7759a30edd9`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ffb4e6dc1ab19b4589ff57e77221320783bce3f50cf263975446e9b166a775`  
		Last Modified: Tue, 12 Nov 2019 02:31:12 GMT  
		Size: 79.2 MB (79246730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e48d3344e9f6d20d253cc9b8c0e62020a424d8d5c1405ea4066f688b01f110`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2105112ea016388d5b835aa32be8f5dfba2e84a40dff93803043b5fcff806`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df92165a3a99469b9cfa588d35c040aa8b7bc8e114422d38cd501397a93563f`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 1.3 MB (1294045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5bbfb4acf75aa2021bd49d72b641da8541333fdd2b67ec378cc391a7aee815`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c192e02a2b87f83721595e911d909829d9aaca448c37c17403a9b63b6a2abc8a`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe1f645884d2346dcef4fe9aaa190fc5ad5614bd3313a541039cd99aaf31b30`  
		Last Modified: Tue, 12 Nov 2019 02:31:02 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded610082ee63d998ec7c77cb724405d7a42b6c42a5c42f8d824c1a23b279384`  
		Last Modified: Tue, 12 Nov 2019 02:31:01 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0`

```console
$ docker pull crate@sha256:f91e0a32ec5ab7bac8f3778b9eb76f285ab11ce0191f583e53fe4ebce24429f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `crate:4.0` - linux; amd64

```console
$ docker pull crate@sha256:e5513005ad7cf7ee33b4cdb0a5e677e64f3e8d056eda50562ee6543eae97221d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352011565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9ab0ca643af2d1e36797cc0f3449f16e8db5dcee5f3742391368a8122e225`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 12 Nov 2019 02:26:04 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Tue, 12 Nov 2019 02:26:05 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Tue, 12 Nov 2019 02:26:05 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Mon, 16 Dec 2019 23:22:08 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.10.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.10.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.10.tar.gz.asc crate-4.0.10.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.10.tar.gz.asc     && tar -xf crate-4.0.10.tar.gz -C /crate --strip-components=1     && rm crate-4.0.10.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Mon, 16 Dec 2019 23:22:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 16 Dec 2019 23:22:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 16 Dec 2019 23:22:12 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 16 Dec 2019 23:22:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2019 23:22:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 16 Dec 2019 23:22:13 GMT
RUN mkdir -p /data/data /data/log
# Mon, 16 Dec 2019 23:22:13 GMT
VOLUME [/data]
# Mon, 16 Dec 2019 23:22:13 GMT
WORKDIR /data
# Mon, 16 Dec 2019 23:22:13 GMT
EXPOSE 4200 4300 5432
# Mon, 16 Dec 2019 23:22:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 16 Dec 2019 23:22:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 16 Dec 2019 23:22:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2019-12-10T13:14:43.986536 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=4.0.10
# Mon, 16 Dec 2019 23:22:14 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Mon, 16 Dec 2019 23:22:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Dec 2019 23:22:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794e274fac32ce9a1fa51077c71a5a03077860c10720987adf900dd957270484`  
		Last Modified: Tue, 12 Nov 2019 02:30:56 GMT  
		Size: 198.1 MB (198127895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a44dfe8d003796a7049dcb6923f2e20d1b4bb030cdf23106d22efff36b353a`  
		Last Modified: Tue, 12 Nov 2019 02:30:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bdd9b9226e19c8ff0f2f7986fc3d126c388cbc39ec0f5ac4503d614fbda7`  
		Last Modified: Mon, 16 Dec 2019 23:22:55 GMT  
		Size: 76.8 MB (76803377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617c1d12b75446d2ee90cb95a6b2d1cc9ed70bfcc7ad3c8840062452f08035f`  
		Last Modified: Mon, 16 Dec 2019 23:22:47 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8d74a34b62cbda1dc6dcb18197ee1a24b7ca0cd7849320b013aca90b450ee7`  
		Last Modified: Mon, 16 Dec 2019 23:22:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8779a4ee84143afd9ae92141153086b787c753d373d1cda3ec4b36aadb8508b1`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 1.3 MB (1294044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad34f552bda0345a689ef2e02a778e8e8d6bc14d8116fe95011ad84a7406579`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd31d4967c89502fb6e32d03ae4c537d6eae3b00e31ab7cad154bf9c33c2637`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d658ffa23a62888b8768321274330de612ca21e0b4bf48e54a08d7c3b862f0b0`  
		Last Modified: Mon, 16 Dec 2019 23:22:45 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1290128f25c2c5f02b590b70e775266693973f7e906de2afde9d287822e358b6`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0.12`

**does not exist** (yet?)

## `crate:4.1`

**does not exist** (yet?)

## `crate:4.1.1`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:338aa792c93a81dee25d9a7f3a29fb4c83c955b59c9e4f356055847349bcf793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e5513005ad7cf7ee33b4cdb0a5e677e64f3e8d056eda50562ee6543eae97221d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352011565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9ab0ca643af2d1e36797cc0f3449f16e8db5dcee5f3742391368a8122e225`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 12 Nov 2019 02:26:04 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Tue, 12 Nov 2019 02:26:05 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Tue, 12 Nov 2019 02:26:05 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Mon, 16 Dec 2019 23:22:08 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.10.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.10.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.10.tar.gz.asc crate-4.0.10.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.10.tar.gz.asc     && tar -xf crate-4.0.10.tar.gz -C /crate --strip-components=1     && rm crate-4.0.10.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Mon, 16 Dec 2019 23:22:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 16 Dec 2019 23:22:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 16 Dec 2019 23:22:12 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 16 Dec 2019 23:22:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2019 23:22:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 16 Dec 2019 23:22:13 GMT
RUN mkdir -p /data/data /data/log
# Mon, 16 Dec 2019 23:22:13 GMT
VOLUME [/data]
# Mon, 16 Dec 2019 23:22:13 GMT
WORKDIR /data
# Mon, 16 Dec 2019 23:22:13 GMT
EXPOSE 4200 4300 5432
# Mon, 16 Dec 2019 23:22:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 16 Dec 2019 23:22:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 16 Dec 2019 23:22:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2019-12-10T13:14:43.986536 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=4.0.10
# Mon, 16 Dec 2019 23:22:14 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Mon, 16 Dec 2019 23:22:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Dec 2019 23:22:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794e274fac32ce9a1fa51077c71a5a03077860c10720987adf900dd957270484`  
		Last Modified: Tue, 12 Nov 2019 02:30:56 GMT  
		Size: 198.1 MB (198127895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a44dfe8d003796a7049dcb6923f2e20d1b4bb030cdf23106d22efff36b353a`  
		Last Modified: Tue, 12 Nov 2019 02:30:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bdd9b9226e19c8ff0f2f7986fc3d126c388cbc39ec0f5ac4503d614fbda7`  
		Last Modified: Mon, 16 Dec 2019 23:22:55 GMT  
		Size: 76.8 MB (76803377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617c1d12b75446d2ee90cb95a6b2d1cc9ed70bfcc7ad3c8840062452f08035f`  
		Last Modified: Mon, 16 Dec 2019 23:22:47 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8d74a34b62cbda1dc6dcb18197ee1a24b7ca0cd7849320b013aca90b450ee7`  
		Last Modified: Mon, 16 Dec 2019 23:22:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8779a4ee84143afd9ae92141153086b787c753d373d1cda3ec4b36aadb8508b1`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 1.3 MB (1294044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad34f552bda0345a689ef2e02a778e8e8d6bc14d8116fe95011ad84a7406579`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd31d4967c89502fb6e32d03ae4c537d6eae3b00e31ab7cad154bf9c33c2637`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d658ffa23a62888b8768321274330de612ca21e0b4bf48e54a08d7c3b862f0b0`  
		Last Modified: Mon, 16 Dec 2019 23:22:45 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1290128f25c2c5f02b590b70e775266693973f7e906de2afde9d287822e358b6`  
		Last Modified: Mon, 16 Dec 2019 23:22:46 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:db0c912f2ffb291abdf1b8ac7032599f0a3d98e1f05af9834b8395666dd5a9b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128570784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f194b7a8010074bbd1dea99993ec8e283b3283be7a20122711e3152938467d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 21 Dec 2018 09:43:06 GMT
ADD file:79419748674899ac7d5d699fe62f837c69d04af3ceaabbb7951c35c2f0ff46fa in / 
# Fri, 21 Dec 2018 09:43:07 GMT
COPY file:a10c133d8d5e9af3a9a1610709d3ed2f85b1507f1ba5745ac12bb495974e3fe6 in /etc/localtime 
# Fri, 21 Dec 2018 09:43:07 GMT
CMD ["/bin/sh"]
# Fri, 21 Dec 2018 13:40:52 GMT
RUN addgroup -g 1000 -S crate     && adduser -u 1000 -G crate -h /crate -S crate
# Fri, 25 Jan 2019 09:53:30 GMT
RUN apk add --no-cache --virtual .crate-rundeps         openjdk8-jre-base         python3         openssl         curl         coreutils     && apk add --no-cache --virtual .build-deps         gnupg         tar     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.1.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.1.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.1.5.tar.gz.asc crate-3.1.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.1.5.tar.gz.asc     && tar -xf crate-3.1.5.tar.gz -C /crate --strip-components=1     && rm crate-3.1.5.tar.gz     && ln -sf /usr/bin/python3 /usr/bin/python     && apk del .build-deps
# Fri, 25 Jan 2019 09:53:43 GMT
RUN apk add --no-cache --virtual .build-deps         gnupg     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2    && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash     && apk del .build-deps
# Fri, 25 Jan 2019 09:53:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Jan 2019 09:53:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 25 Jan 2019 09:53:50 GMT
HEALTHCHECK &{["CMD-SHELL" "curl --max-time 25 $(hostname):4200 || exit 1"] "30s" "30s" "0s" '\x00'}
# Fri, 25 Jan 2019 09:53:57 GMT
RUN mkdir -p /data/data /data/log
# Fri, 25 Jan 2019 09:53:58 GMT
VOLUME [/data]
# Fri, 25 Jan 2019 09:54:01 GMT
WORKDIR /data
# Fri, 25 Jan 2019 09:54:03 GMT
EXPOSE 4200 4300 5432
# Fri, 25 Jan 2019 09:54:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2019-01-22T17:02:01.628483081+00:00 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.1.5
# Fri, 25 Jan 2019 09:54:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 25 Jan 2019 09:54:08 GMT
COPY --chown=1000:0file:0d0763ba6bbc9b78b4a05b228e1f3ca6b2b3b56aefaf888ab848f021062291d1 in /crate/config/log4j2.properties 
# Fri, 25 Jan 2019 09:54:08 GMT
COPY file:45928eb9f61bad7db8a236ab07cde77661e3e034d86ecfba093f320e019b3ce0 in /docker-entrypoint.sh 
# Fri, 25 Jan 2019 09:54:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 25 Jan 2019 09:54:13 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e3c488b39803d9194cf010f6127b1121d5387b90a1562d44b50b749d0e7a69bf`  
		Last Modified: Fri, 21 Dec 2018 09:43:51 GMT  
		Size: 2.1 MB (2099839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a63128803b1ea223f87244cb8d3faa97817f6cf3ca8249e485430218758510`  
		Last Modified: Fri, 21 Dec 2018 09:43:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6e4828a3e9f80bfa761b39062e4481c11b4a610152a814acd32573231fa99`  
		Last Modified: Fri, 21 Dec 2018 13:42:11 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0e67bbf3f48cc5272f52f25ca390d32d7129326881f72227fa77c036063c0d`  
		Last Modified: Fri, 25 Jan 2019 09:55:07 GMT  
		Size: 125.0 MB (125011209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7f21460e9575c38dc2e949517a38a8879a2cd80160ec7ab0c0bd58aed14fc0`  
		Last Modified: Fri, 25 Jan 2019 09:54:36 GMT  
		Size: 1.5 MB (1456441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da11ea425af1731ea21a870fa115175477cae145c8ade3c1daaf9e87bf216f13`  
		Last Modified: Fri, 25 Jan 2019 09:54:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e901e4006cebfb1689df93628a914d428008bc5a4998a3794fcb564853083d3`  
		Last Modified: Fri, 25 Jan 2019 09:54:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aff0b367ba9ee7651f99121048f8d6d970a02d5634af435b7e1cd68f238c6c6`  
		Last Modified: Fri, 25 Jan 2019 09:54:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0c2d26d4648beea5d96e217db832b78f33579544be71ffe03f3dfbe30f6fe4`  
		Last Modified: Fri, 25 Jan 2019 09:54:36 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
