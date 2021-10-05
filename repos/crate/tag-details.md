<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:3.3`](#crate33)
-	[`crate:3.3.5`](#crate335)
-	[`crate:4.0`](#crate40)
-	[`crate:4.0.12`](#crate4012)
-	[`crate:4.1`](#crate41)
-	[`crate:4.1.8`](#crate418)
-	[`crate:4.2`](#crate42)
-	[`crate:4.2.7`](#crate427)
-	[`crate:4.3`](#crate43)
-	[`crate:4.3.4`](#crate434)
-	[`crate:4.4`](#crate44)
-	[`crate:4.4.3`](#crate443)
-	[`crate:4.5`](#crate45)
-	[`crate:4.5.5`](#crate455)
-	[`crate:4.6`](#crate46)
-	[`crate:4.6.4`](#crate464)
-	[`crate:latest`](#cratelatest)

## `crate:3.3`

```console
$ docker pull crate@sha256:895ef6425e65fbfa33add64a00b35f9417ecd8e02ac15118203840e74d8a93c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:3.3` - linux; amd64

```console
$ docker pull crate@sha256:bfc40b82e769c4db403ce8248173c7d19ee4086892983d957dfd09432eb42108
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346104048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc20c49302424e7f186f8a48d065c21203c9e6b1e0648200419d97ffd4c6209`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:45:19 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:45:19 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Wed, 15 Sep 2021 18:45:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:45:47 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:45:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:45:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:45:52 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:45:52 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:45:52 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:45:52 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:45:52 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Wed, 15 Sep 2021 18:45:53 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:45:53 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0e044482b3d240288e224684f247ade975d7d76da11f8eb433c5ccb173303e`  
		Last Modified: Wed, 15 Sep 2021 18:50:58 GMT  
		Size: 188.1 MB (188101473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747c2aaeacb9824d83abbf999141d608b042a8d47cffa202cc1564a6c3aca055`  
		Last Modified: Wed, 15 Sep 2021 18:50:42 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6456300f4ce458352327aec65502220dad3aa03aac0ab064e2764c02ab1cc`  
		Last Modified: Wed, 15 Sep 2021 18:50:51 GMT  
		Size: 80.6 MB (80605664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47792dae1bf3f855656b97ad592882a320e7f969451df66c54528c2c3df9cb9d`  
		Last Modified: Wed, 15 Sep 2021 18:50:42 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3f82031ff4331de824cb06d0c01f694e7ddfc0f4622e79c7fd9cecbe58bffe`  
		Last Modified: Wed, 15 Sep 2021 18:50:43 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65eecb1cee79a4b2b89cf53d03956070bbc715070310747aa797861709e313a`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 1.3 MB (1294155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9ec8fecce8841015edb5f631c56de023fd6993ce32b48548b88e682079dc6`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7b46f209e7a36f75e4f81d7097ecd80a018a27cf9271261a89fd82f080d74f`  
		Last Modified: Wed, 15 Sep 2021 18:50:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9687883824cff91519e5863e6e3fa3655af648637c510c9dd9f9ad9e9e004f2`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d0a81fbac281ebc6451d129a0ece22ef5c82c3de95fda74ab182ea1367ac24`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:3.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c0604d922ee02767a148be908ecd0f999dedf3f1721c847400053248e03ebc15
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377488804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3353827aa147cf76315053fcdc3ffcc85891ade5e8aaa257de81352078fe8a92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:13:33 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:13:34 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Wed, 15 Sep 2021 18:13:34 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:14:09 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:14:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:14:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:14:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:14:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:14:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:14:13 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:14:13 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:14:13 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:14:13 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:14:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:14:13 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:14:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Wed, 15 Sep 2021 18:14:14 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:14:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:14:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d55d209616688d128c0966f26f6d4cde0525a1646481496e39acdd6fbdf50b`  
		Last Modified: Wed, 15 Sep 2021 18:19:16 GMT  
		Size: 188.1 MB (188101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100e807921bbb4f3260c08d89948d73d7449f966450aa46e6d9d9e4794dea8b5`  
		Last Modified: Wed, 15 Sep 2021 18:18:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6acbe39bd97bd8703f293f243124e7c80dbaaa76ab7cfa82c957dcb94931a7`  
		Last Modified: Wed, 15 Sep 2021 18:19:06 GMT  
		Size: 79.7 MB (79712653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ce0561df708f96093882b699f28d84f0fac624d5fae911334abf4749a955a3`  
		Last Modified: Wed, 15 Sep 2021 18:18:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a862272790d26155388bcfced03f2a329ef733d653ad7e81b94b8dee1ca2694`  
		Last Modified: Wed, 15 Sep 2021 18:18:57 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf5d8aefb5f8a9e428f234f6441e0024633085901ced16a83e267a482437c5f`  
		Last Modified: Wed, 15 Sep 2021 18:18:56 GMT  
		Size: 1.3 MB (1294154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fdd0bded723ecfc3c9e1916cf4ac436ee218156821bbe008c840fc9b97b08`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef69b76ba40b9f76f325cf726120c3ea000fa5be01923ac857e23d254b95934c`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fcc778aeaee9702775dbde65e3d1723ee3641aa02db91eda1e7aa40e6666e`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dcff42247f23bd06b18f626db1c07ffebb44f55329c1fdb6bfabbec25d6fd0`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:3.3.5`

```console
$ docker pull crate@sha256:895ef6425e65fbfa33add64a00b35f9417ecd8e02ac15118203840e74d8a93c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:3.3.5` - linux; amd64

```console
$ docker pull crate@sha256:bfc40b82e769c4db403ce8248173c7d19ee4086892983d957dfd09432eb42108
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346104048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc20c49302424e7f186f8a48d065c21203c9e6b1e0648200419d97ffd4c6209`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:45:19 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:45:19 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Wed, 15 Sep 2021 18:45:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:45:47 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:45:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:45:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:45:52 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:45:52 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:45:52 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:45:52 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:45:52 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Wed, 15 Sep 2021 18:45:53 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:45:53 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0e044482b3d240288e224684f247ade975d7d76da11f8eb433c5ccb173303e`  
		Last Modified: Wed, 15 Sep 2021 18:50:58 GMT  
		Size: 188.1 MB (188101473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747c2aaeacb9824d83abbf999141d608b042a8d47cffa202cc1564a6c3aca055`  
		Last Modified: Wed, 15 Sep 2021 18:50:42 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6456300f4ce458352327aec65502220dad3aa03aac0ab064e2764c02ab1cc`  
		Last Modified: Wed, 15 Sep 2021 18:50:51 GMT  
		Size: 80.6 MB (80605664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47792dae1bf3f855656b97ad592882a320e7f969451df66c54528c2c3df9cb9d`  
		Last Modified: Wed, 15 Sep 2021 18:50:42 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3f82031ff4331de824cb06d0c01f694e7ddfc0f4622e79c7fd9cecbe58bffe`  
		Last Modified: Wed, 15 Sep 2021 18:50:43 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65eecb1cee79a4b2b89cf53d03956070bbc715070310747aa797861709e313a`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 1.3 MB (1294155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9ec8fecce8841015edb5f631c56de023fd6993ce32b48548b88e682079dc6`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7b46f209e7a36f75e4f81d7097ecd80a018a27cf9271261a89fd82f080d74f`  
		Last Modified: Wed, 15 Sep 2021 18:50:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9687883824cff91519e5863e6e3fa3655af648637c510c9dd9f9ad9e9e004f2`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d0a81fbac281ebc6451d129a0ece22ef5c82c3de95fda74ab182ea1367ac24`  
		Last Modified: Wed, 15 Sep 2021 18:50:40 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:3.3.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c0604d922ee02767a148be908ecd0f999dedf3f1721c847400053248e03ebc15
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377488804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3353827aa147cf76315053fcdc3ffcc85891ade5e8aaa257de81352078fe8a92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:13:33 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:13:34 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Wed, 15 Sep 2021 18:13:34 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:14:09 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:14:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:14:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:14:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:14:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:14:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:14:13 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:14:13 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:14:13 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:14:13 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:14:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:14:13 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:14:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Wed, 15 Sep 2021 18:14:14 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:14:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:14:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d55d209616688d128c0966f26f6d4cde0525a1646481496e39acdd6fbdf50b`  
		Last Modified: Wed, 15 Sep 2021 18:19:16 GMT  
		Size: 188.1 MB (188101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100e807921bbb4f3260c08d89948d73d7449f966450aa46e6d9d9e4794dea8b5`  
		Last Modified: Wed, 15 Sep 2021 18:18:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6acbe39bd97bd8703f293f243124e7c80dbaaa76ab7cfa82c957dcb94931a7`  
		Last Modified: Wed, 15 Sep 2021 18:19:06 GMT  
		Size: 79.7 MB (79712653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ce0561df708f96093882b699f28d84f0fac624d5fae911334abf4749a955a3`  
		Last Modified: Wed, 15 Sep 2021 18:18:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a862272790d26155388bcfced03f2a329ef733d653ad7e81b94b8dee1ca2694`  
		Last Modified: Wed, 15 Sep 2021 18:18:57 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf5d8aefb5f8a9e428f234f6441e0024633085901ced16a83e267a482437c5f`  
		Last Modified: Wed, 15 Sep 2021 18:18:56 GMT  
		Size: 1.3 MB (1294154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fdd0bded723ecfc3c9e1916cf4ac436ee218156821bbe008c840fc9b97b08`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef69b76ba40b9f76f325cf726120c3ea000fa5be01923ac857e23d254b95934c`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fcc778aeaee9702775dbde65e3d1723ee3641aa02db91eda1e7aa40e6666e`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dcff42247f23bd06b18f626db1c07ffebb44f55329c1fdb6bfabbec25d6fd0`  
		Last Modified: Wed, 15 Sep 2021 18:18:55 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0`

```console
$ docker pull crate@sha256:c9198c51a000886ff8ef94768f6df2767138956bd690aae1f416eadeddf50f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.0` - linux; amd64

```console
$ docker pull crate@sha256:023a9ca9b9e1d94d2ef6d656e907c7ec724ea2ef5e5f90409ccdb1d34282c59b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339601325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e26029cccf8119ad4027ef137d83c79de1bece17cbed79c8a47bf04d455a2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:44:37 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:44:38 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Wed, 15 Sep 2021 18:44:39 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:45:02 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:45:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:05 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:45:05 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:45:05 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:45:06 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:45:06 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:45:06 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:45:07 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:45:07 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Wed, 15 Sep 2021 18:45:08 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:45:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:45:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f76998ac4a5a9c7f49fb7c8996c566e73bacf6d7e89ba942fb7502e83debcb`  
		Last Modified: Wed, 15 Sep 2021 18:50:29 GMT  
		Size: 198.1 MB (198127620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8946104cbe997bb27948a18ab9f114ff08ee18e76d279025517ff3bbd5ac93f4`  
		Last Modified: Wed, 15 Sep 2021 18:50:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4a66e82bca0fab3011e8161f9f95030fe0d3a441d76d1be21211179e9bd8e`  
		Last Modified: Wed, 15 Sep 2021 18:50:19 GMT  
		Size: 64.1 MB (64076800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b19388b08a92bfae0491dec3c66b86061c2db3696a032b4c608712b40edf380`  
		Last Modified: Wed, 15 Sep 2021 18:50:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47d7dbff92094fc5eefad873d0c78bbb44b85e73bdc630a5e28012898f9407b`  
		Last Modified: Wed, 15 Sep 2021 18:50:13 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cb88b1493976361d81baa74adb5abceaa3178ed2bf3ce87b1343e00a9e1124`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 1.3 MB (1294150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff41c9d783c4cb9dea669196bcba59750e071a7e9883ef6e28412d8bff1b2644`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6633eff95a7165ffa028562881394e6b91998c6ff75071b04e4ec561fee5f2a6`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166ed56e6596e398825b40fad37f319d8a1fbec26675fd2baeffbd289c891de3`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a2623fe3aa39d7d0442fae1e848798bd46924b7bb1051325d15ebbbf99a95f`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:51bf1cc877c18b63f760d539fea94fc15a10460bd3162b619904a0d213dcb5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371411914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8454f08a9113395399f4fb187af925eeb47098d42aec413cd5388268101b88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:12:35 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:12:36 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Wed, 15 Sep 2021 18:12:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:13:03 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:13:04 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:13:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:13:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:13:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:13:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:13:07 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:13:07 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:13:07 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:13:08 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:13:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:13:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:13:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Wed, 15 Sep 2021 18:13:08 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:13:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4a151204dc26fbafee14be41c412cb3acbe875e1a7951408c0f56c2a828230`  
		Last Modified: Wed, 15 Sep 2021 18:18:42 GMT  
		Size: 198.1 MB (198127737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde5f8d7221b3e6f9da6009e04ea719efeb1cc36d394af1acbe0c55a604871c`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba1b12a0474acb64639ff1dd8a6e858010964c3d09adb8f9a4c57964185541`  
		Last Modified: Wed, 15 Sep 2021 18:18:29 GMT  
		Size: 63.6 MB (63609467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cd7f69c0fe03d6ac7d85874826dfdb4ba641c493cdd812278561c2fd6fa66`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7eb94ea0274ad0f53cf17aa5d925ddf1567c6446c2a78362ae200144a6e023`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249f12104d25f68817b56ee123d37aa48b6b507d3dabd3852c16ecfca2272af3`  
		Last Modified: Wed, 15 Sep 2021 18:18:21 GMT  
		Size: 1.3 MB (1294159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fcda660b356d09731c7d7354ed653e454ee0b5d3a3ba5db6069efef9dcebbd`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314f4e642629660554f58273d2976ea65d7586cf8e33da2d72a99faadf182c95`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531b746650f37d83ef4e6fb342be0c138e1dd2a6232ea1ee95e8bb83bdaf0d4f`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf140d3ecfcb2767b1b13c6188aa211237166c0073b2c8a129b08286ca1b838`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0.12`

```console
$ docker pull crate@sha256:c9198c51a000886ff8ef94768f6df2767138956bd690aae1f416eadeddf50f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.0.12` - linux; amd64

```console
$ docker pull crate@sha256:023a9ca9b9e1d94d2ef6d656e907c7ec724ea2ef5e5f90409ccdb1d34282c59b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339601325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e26029cccf8119ad4027ef137d83c79de1bece17cbed79c8a47bf04d455a2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:44:37 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:44:38 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Wed, 15 Sep 2021 18:44:39 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:45:02 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:45:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:05 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:45:05 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:45:05 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:45:06 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:45:06 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:45:06 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:45:07 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:45:07 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:45:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:45:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Wed, 15 Sep 2021 18:45:08 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:45:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:45:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f76998ac4a5a9c7f49fb7c8996c566e73bacf6d7e89ba942fb7502e83debcb`  
		Last Modified: Wed, 15 Sep 2021 18:50:29 GMT  
		Size: 198.1 MB (198127620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8946104cbe997bb27948a18ab9f114ff08ee18e76d279025517ff3bbd5ac93f4`  
		Last Modified: Wed, 15 Sep 2021 18:50:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4a66e82bca0fab3011e8161f9f95030fe0d3a441d76d1be21211179e9bd8e`  
		Last Modified: Wed, 15 Sep 2021 18:50:19 GMT  
		Size: 64.1 MB (64076800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b19388b08a92bfae0491dec3c66b86061c2db3696a032b4c608712b40edf380`  
		Last Modified: Wed, 15 Sep 2021 18:50:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47d7dbff92094fc5eefad873d0c78bbb44b85e73bdc630a5e28012898f9407b`  
		Last Modified: Wed, 15 Sep 2021 18:50:13 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cb88b1493976361d81baa74adb5abceaa3178ed2bf3ce87b1343e00a9e1124`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 1.3 MB (1294150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff41c9d783c4cb9dea669196bcba59750e071a7e9883ef6e28412d8bff1b2644`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6633eff95a7165ffa028562881394e6b91998c6ff75071b04e4ec561fee5f2a6`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166ed56e6596e398825b40fad37f319d8a1fbec26675fd2baeffbd289c891de3`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a2623fe3aa39d7d0442fae1e848798bd46924b7bb1051325d15ebbbf99a95f`  
		Last Modified: Wed, 15 Sep 2021 18:50:11 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.0.12` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:51bf1cc877c18b63f760d539fea94fc15a10460bd3162b619904a0d213dcb5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371411914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8454f08a9113395399f4fb187af925eeb47098d42aec413cd5388268101b88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:12:35 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:12:36 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Wed, 15 Sep 2021 18:12:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:13:03 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 15 Sep 2021 18:13:04 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:13:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:13:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:13:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:13:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:13:07 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:13:07 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:13:07 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:13:08 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:13:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:13:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:13:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Wed, 15 Sep 2021 18:13:08 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:13:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4a151204dc26fbafee14be41c412cb3acbe875e1a7951408c0f56c2a828230`  
		Last Modified: Wed, 15 Sep 2021 18:18:42 GMT  
		Size: 198.1 MB (198127737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde5f8d7221b3e6f9da6009e04ea719efeb1cc36d394af1acbe0c55a604871c`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba1b12a0474acb64639ff1dd8a6e858010964c3d09adb8f9a4c57964185541`  
		Last Modified: Wed, 15 Sep 2021 18:18:29 GMT  
		Size: 63.6 MB (63609467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cd7f69c0fe03d6ac7d85874826dfdb4ba641c493cdd812278561c2fd6fa66`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7eb94ea0274ad0f53cf17aa5d925ddf1567c6446c2a78362ae200144a6e023`  
		Last Modified: Wed, 15 Sep 2021 18:18:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249f12104d25f68817b56ee123d37aa48b6b507d3dabd3852c16ecfca2272af3`  
		Last Modified: Wed, 15 Sep 2021 18:18:21 GMT  
		Size: 1.3 MB (1294159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fcda660b356d09731c7d7354ed653e454ee0b5d3a3ba5db6069efef9dcebbd`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314f4e642629660554f58273d2976ea65d7586cf8e33da2d72a99faadf182c95`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531b746650f37d83ef4e6fb342be0c138e1dd2a6232ea1ee95e8bb83bdaf0d4f`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf140d3ecfcb2767b1b13c6188aa211237166c0073b2c8a129b08286ca1b838`  
		Last Modified: Wed, 15 Sep 2021 18:18:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.1`

```console
$ docker pull crate@sha256:c5aed7744c5fcabfd610ffc500c57f089544c7b49373cad5fa86050fc4bec56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.1` - linux; amd64

```console
$ docker pull crate@sha256:b6a73e1a4664dc51f8fadd2ce315b7cb69ebb8e688517b06ebaf79662f85883f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352665970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a152e61c14b2aac693602db17a9321cf2043243e0f40643590af1a7678033`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:43:46 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:43:47 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 15 Sep 2021 18:43:48 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:44:13 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:44:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:44:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:44:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:44:17 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:44:17 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:44:17 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:44:17 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:44:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:44:18 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:44:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Wed, 15 Sep 2021 18:44:18 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:44:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324302278d02e55d7511c3e6bfec093ca6c9093e5ca747ec172e55c2240dc04c`  
		Last Modified: Wed, 15 Sep 2021 18:50:00 GMT  
		Size: 196.4 MB (196423306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d743c71fd4fcb4f5a5923440f6a9b77b80279276851877f2b603ad4cbf32c22f`  
		Last Modified: Wed, 15 Sep 2021 18:49:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a1e83e2285e41c0a677cec6419f9bcb7f15fff8782961378ef92f9d775125`  
		Last Modified: Wed, 15 Sep 2021 18:49:53 GMT  
		Size: 78.8 MB (78846970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f5576063cf53ab53f99ea320d61269ade335620dce0674717318fa0c87d0c0`  
		Last Modified: Wed, 15 Sep 2021 18:49:43 GMT  
		Size: 1.3 MB (1294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5096100c7396787a214a622aed965e7beea89c5304a3df545fd3920efafcb0e1`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fcd8ec9dc28af3e85727eea8e6609f459f2979e2abc4f752067114f42a5803`  
		Last Modified: Wed, 15 Sep 2021 18:49:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceebbc5574a8563656f73f7cadea7a10b5af13a62b12f07fb32b02183a245393`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f74414a5b96fabf39a48490b659b3ed271b613988288faec6fc4e95c1658e7`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5f93dcc9d2bbc0711090ac4c4736fcc0ebe05de7abe20334a4cf2c1df73a93e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 MB (384066813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458fc92e636f4b8fc3c7d5c12193e2a966fa4c082a3ea8b4b657746ed0c53bfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:11:13 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:11:14 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 15 Sep 2021 18:11:14 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:11:54 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:11:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:11:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:11:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:11:59 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:11:59 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:12:00 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:12:00 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:12:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:12:00 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:12:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Wed, 15 Sep 2021 18:12:01 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:12:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:12:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da61b3c589bcc9f092c865bc7ae5c83f71d08b3547a87de8eb38f323f108008`  
		Last Modified: Wed, 15 Sep 2021 18:18:07 GMT  
		Size: 196.4 MB (196423268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf980216257e9e5b8da68910a926242c63c463f02e08fb14d0638917f0c5f05`  
		Last Modified: Wed, 15 Sep 2021 18:17:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33022443704250c675804600137b163ec3cdaa6efb9b58520e266ab6b7c775`  
		Last Modified: Wed, 15 Sep 2021 18:17:57 GMT  
		Size: 78.0 MB (77970067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66803cb7ad6f559d3303143e1e96f7e749caa764c4eadaa3c92c33e0b530f0d`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 1.3 MB (1294154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ec37d3daed3173bbcc9289358e8825371a7f2687525c50f7aeb9c6bd0c81bc`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e68be5b260c923088196719cd48d39627d3a98eb6aee2eeb9b317cc01742957`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf56fad18dc8c02918153497c837d846851713c8d66c8eee803d8de00291e2c`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1726f94a47d98fe886ba827598d3a0cc7f845d12fc5f47159628a3c2fd26d6`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.1.8`

```console
$ docker pull crate@sha256:c5aed7744c5fcabfd610ffc500c57f089544c7b49373cad5fa86050fc4bec56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.1.8` - linux; amd64

```console
$ docker pull crate@sha256:b6a73e1a4664dc51f8fadd2ce315b7cb69ebb8e688517b06ebaf79662f85883f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352665970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a152e61c14b2aac693602db17a9321cf2043243e0f40643590af1a7678033`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:43:46 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:43:47 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 15 Sep 2021 18:43:48 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:44:13 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:44:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:44:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:44:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:44:17 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:44:17 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:44:17 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:44:17 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:44:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:44:18 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:44:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Wed, 15 Sep 2021 18:44:18 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:44:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324302278d02e55d7511c3e6bfec093ca6c9093e5ca747ec172e55c2240dc04c`  
		Last Modified: Wed, 15 Sep 2021 18:50:00 GMT  
		Size: 196.4 MB (196423306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d743c71fd4fcb4f5a5923440f6a9b77b80279276851877f2b603ad4cbf32c22f`  
		Last Modified: Wed, 15 Sep 2021 18:49:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a1e83e2285e41c0a677cec6419f9bcb7f15fff8782961378ef92f9d775125`  
		Last Modified: Wed, 15 Sep 2021 18:49:53 GMT  
		Size: 78.8 MB (78846970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f5576063cf53ab53f99ea320d61269ade335620dce0674717318fa0c87d0c0`  
		Last Modified: Wed, 15 Sep 2021 18:49:43 GMT  
		Size: 1.3 MB (1294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5096100c7396787a214a622aed965e7beea89c5304a3df545fd3920efafcb0e1`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fcd8ec9dc28af3e85727eea8e6609f459f2979e2abc4f752067114f42a5803`  
		Last Modified: Wed, 15 Sep 2021 18:49:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceebbc5574a8563656f73f7cadea7a10b5af13a62b12f07fb32b02183a245393`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f74414a5b96fabf39a48490b659b3ed271b613988288faec6fc4e95c1658e7`  
		Last Modified: Wed, 15 Sep 2021 18:49:42 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.1.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5f93dcc9d2bbc0711090ac4c4736fcc0ebe05de7abe20334a4cf2c1df73a93e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 MB (384066813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458fc92e636f4b8fc3c7d5c12193e2a966fa4c082a3ea8b4b657746ed0c53bfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:11:13 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 15 Sep 2021 18:11:14 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 15 Sep 2021 18:11:14 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 15 Sep 2021 18:11:54 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:11:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:11:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:11:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:11:59 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:11:59 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:12:00 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:12:00 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:12:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:12:00 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:12:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Wed, 15 Sep 2021 18:12:01 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 15 Sep 2021 18:12:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:12:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da61b3c589bcc9f092c865bc7ae5c83f71d08b3547a87de8eb38f323f108008`  
		Last Modified: Wed, 15 Sep 2021 18:18:07 GMT  
		Size: 196.4 MB (196423268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf980216257e9e5b8da68910a926242c63c463f02e08fb14d0638917f0c5f05`  
		Last Modified: Wed, 15 Sep 2021 18:17:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33022443704250c675804600137b163ec3cdaa6efb9b58520e266ab6b7c775`  
		Last Modified: Wed, 15 Sep 2021 18:17:57 GMT  
		Size: 78.0 MB (77970067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66803cb7ad6f559d3303143e1e96f7e749caa764c4eadaa3c92c33e0b530f0d`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 1.3 MB (1294154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ec37d3daed3173bbcc9289358e8825371a7f2687525c50f7aeb9c6bd0c81bc`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e68be5b260c923088196719cd48d39627d3a98eb6aee2eeb9b317cc01742957`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf56fad18dc8c02918153497c837d846851713c8d66c8eee803d8de00291e2c`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1726f94a47d98fe886ba827598d3a0cc7f845d12fc5f47159628a3c2fd26d6`  
		Last Modified: Wed, 15 Sep 2021 18:17:46 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.2`

```console
$ docker pull crate@sha256:65cc54813a6b91a275c962c8d059e842824d6d669d64305c51d7b052f61b7460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.2` - linux; amd64

```console
$ docker pull crate@sha256:decef05a6d8df34332b8d86f1d9cf56c6a141333856465f35cb6fa7d846674b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334409501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a176db28ea480b87622ad04c061c5b0c34bb8d77efff53220c3e707a46cf78e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:43:29 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:43:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:43:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:43:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:43:33 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:43:34 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:43:34 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:43:34 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:43:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:43:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:43:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Wed, 15 Sep 2021 18:43:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:43:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:43:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f07dd2d491263b2583fce62ed914659ff179ea92b8b892a5b168990aa6f2e99`  
		Last Modified: Wed, 15 Sep 2021 18:49:32 GMT  
		Size: 256.7 MB (256740381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19de006528e30c4c3cc4b94659f4b39d8997c1a2f092ccecbb212bd49c823db5`  
		Last Modified: Wed, 15 Sep 2021 18:49:09 GMT  
		Size: 1.6 MB (1567823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e81490d7ccc8c181dfce90ac9f960ddf1a1c04ef2d88452ce43100ceaa6e5`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dc9b60f8483acae1d68d05e6a6b5d0cc04349df9bd54735cf77d9b452875da`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befbc6604546640bfd2c21a755f76e337a9d22dceadb52b481adc24aaeaa9c7e`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d46d6e574416662a735c3aea2524cf5eb9db076afc147fc13fb73ad4dedabc`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3f0f5a816bce88d3147d7262439f69ba3266d35a1ca1e6cccf242699cb8a9ce0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363219205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46039e014fed9307af29124cf35c70c252cbd4693da3302a999a0974e0122bf2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:10:40 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:10:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:10:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:10:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:10:44 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:10:44 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:10:45 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:10:45 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:10:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:10:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:10:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Wed, 15 Sep 2021 18:10:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:10:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:10:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962ab34d8e29a4822779f10a8f7ac80dcfa36575decdbf502f3b893760f1354d`  
		Last Modified: Wed, 15 Sep 2021 18:17:31 GMT  
		Size: 253.3 MB (253272290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43285cae40804eefbc4b4b310352ea0d0e166b65c4119bc4f10aed0b8db26075`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 1.6 MB (1567830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb002f543e9094bbc8cd1ace947ca5b28bbbfd4a450b9b3c8e91a5911c6f22e`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48806f949522459e5581aff305ec28da7ea1351fa2f68e82967cd8e430447f7`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2378a3f0de94b87253cdf5de90863a3e2817989df6f729a87283b8ef8b93d`  
		Last Modified: Wed, 15 Sep 2021 18:17:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc5b21baf532730ca69a50835850054acb4783643be2d73db8d6b0c929854c7`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.2.7`

```console
$ docker pull crate@sha256:65cc54813a6b91a275c962c8d059e842824d6d669d64305c51d7b052f61b7460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.2.7` - linux; amd64

```console
$ docker pull crate@sha256:decef05a6d8df34332b8d86f1d9cf56c6a141333856465f35cb6fa7d846674b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334409501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a176db28ea480b87622ad04c061c5b0c34bb8d77efff53220c3e707a46cf78e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:43:29 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:43:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:43:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:43:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:43:33 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:43:34 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:43:34 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:43:34 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:43:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:43:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:43:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Wed, 15 Sep 2021 18:43:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:43:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:43:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f07dd2d491263b2583fce62ed914659ff179ea92b8b892a5b168990aa6f2e99`  
		Last Modified: Wed, 15 Sep 2021 18:49:32 GMT  
		Size: 256.7 MB (256740381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19de006528e30c4c3cc4b94659f4b39d8997c1a2f092ccecbb212bd49c823db5`  
		Last Modified: Wed, 15 Sep 2021 18:49:09 GMT  
		Size: 1.6 MB (1567823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e81490d7ccc8c181dfce90ac9f960ddf1a1c04ef2d88452ce43100ceaa6e5`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dc9b60f8483acae1d68d05e6a6b5d0cc04349df9bd54735cf77d9b452875da`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befbc6604546640bfd2c21a755f76e337a9d22dceadb52b481adc24aaeaa9c7e`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d46d6e574416662a735c3aea2524cf5eb9db076afc147fc13fb73ad4dedabc`  
		Last Modified: Wed, 15 Sep 2021 18:49:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.2.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3f0f5a816bce88d3147d7262439f69ba3266d35a1ca1e6cccf242699cb8a9ce0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363219205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46039e014fed9307af29124cf35c70c252cbd4693da3302a999a0974e0122bf2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:10:40 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:10:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:10:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:10:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:10:44 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:10:44 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:10:45 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:10:45 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:10:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:10:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:10:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Wed, 15 Sep 2021 18:10:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:10:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:10:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962ab34d8e29a4822779f10a8f7ac80dcfa36575decdbf502f3b893760f1354d`  
		Last Modified: Wed, 15 Sep 2021 18:17:31 GMT  
		Size: 253.3 MB (253272290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43285cae40804eefbc4b4b310352ea0d0e166b65c4119bc4f10aed0b8db26075`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 1.6 MB (1567830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb002f543e9094bbc8cd1ace947ca5b28bbbfd4a450b9b3c8e91a5911c6f22e`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48806f949522459e5581aff305ec28da7ea1351fa2f68e82967cd8e430447f7`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2378a3f0de94b87253cdf5de90863a3e2817989df6f729a87283b8ef8b93d`  
		Last Modified: Wed, 15 Sep 2021 18:17:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc5b21baf532730ca69a50835850054acb4783643be2d73db8d6b0c929854c7`  
		Last Modified: Wed, 15 Sep 2021 18:17:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.3`

```console
$ docker pull crate@sha256:8971b6395369aaedc84eadc81ae79bdbba0a56521e0b4ae64a64758d3a80ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.3` - linux; amd64

```console
$ docker pull crate@sha256:6b11bfd5fea84de8716bedd09a8f4d4b5dbd254fa02b6643a53e8da0459a6d7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333120845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ecac8429328507a44ac743eea77bb055db6e48bd595ca4a1e9170b54a1038`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:42:17 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:42:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:42:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:42:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:42:23 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:42:24 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:42:24 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:42:24 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:42:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:42:25 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:42:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Wed, 15 Sep 2021 18:42:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:42:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:42:26 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78717aec970ce9ea7b9d2d6ec3e79d5cba90428d3925d80fbbcae07ba4bbe5d`  
		Last Modified: Wed, 15 Sep 2021 18:48:55 GMT  
		Size: 255.5 MB (255451713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1f162a3a683fafe1c21dc32a0470b54c2fc15d36af56fbe0b0564f0709d341`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 1.6 MB (1567833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebae486e7e140b715ba021003e1fbe270a486cc4d43d72a63d496f59de1fd11`  
		Last Modified: Wed, 15 Sep 2021 18:48:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6c4d94c0744743ec9b0ef6eaebf5c762b1177d60b69e90bcd53e6d022a3761`  
		Last Modified: Wed, 15 Sep 2021 18:48:32 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6865ddeca380112eb05cd73aa051b641679ee53c53c1518f8a65ec43413e19c`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976c7967156aea258deb3e7fb1ab43f6cf27ee679271fa8a7621ff731d753cee`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4f38ae124d0efb2392c4746560aa4dbd6be7de79c98c0c6b01d3c1805f339176
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362066251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a6eea957e927ab8f3b6c59bc55b761506bf757df5c835b16557f6d8eb0ea27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:09:34 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:09:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:09:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:09:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:09:43 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:09:43 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:09:44 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:09:44 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:09:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:09:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:09:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Wed, 15 Sep 2021 18:09:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:09:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:09:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa3a82789006023c6b746e3f23a75b4c230873809340254f4785d1f77097725`  
		Last Modified: Wed, 15 Sep 2021 18:16:50 GMT  
		Size: 252.1 MB (252119353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da807595a8b2a47dc84f1a48745d5c5e9d0e96a4cacf0c5a362273519a1aa783`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 1.6 MB (1567819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77975723368b5d9b05b5c84ec3e477b3a32c817daa1c784c7c4ff81abf1f6ce7`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a66907876f27dad084e239771168e2c64543ae1b9ff1c144f363c4a87b980`  
		Last Modified: Wed, 15 Sep 2021 18:16:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e3c070a33a70c801d61edabf6ee388904fa1966f86c63ade12c0b778da5b2`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0687ec88c4740cb59d7cfb9d9705167478b75db03b896937fe38f6a6a815b5e5`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.3.4`

```console
$ docker pull crate@sha256:8971b6395369aaedc84eadc81ae79bdbba0a56521e0b4ae64a64758d3a80ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.3.4` - linux; amd64

```console
$ docker pull crate@sha256:6b11bfd5fea84de8716bedd09a8f4d4b5dbd254fa02b6643a53e8da0459a6d7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333120845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ecac8429328507a44ac743eea77bb055db6e48bd595ca4a1e9170b54a1038`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:42:17 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:42:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:42:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:42:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:42:23 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:42:24 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:42:24 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:42:24 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:42:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:42:25 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:42:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Wed, 15 Sep 2021 18:42:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:42:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:42:26 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78717aec970ce9ea7b9d2d6ec3e79d5cba90428d3925d80fbbcae07ba4bbe5d`  
		Last Modified: Wed, 15 Sep 2021 18:48:55 GMT  
		Size: 255.5 MB (255451713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1f162a3a683fafe1c21dc32a0470b54c2fc15d36af56fbe0b0564f0709d341`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 1.6 MB (1567833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebae486e7e140b715ba021003e1fbe270a486cc4d43d72a63d496f59de1fd11`  
		Last Modified: Wed, 15 Sep 2021 18:48:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6c4d94c0744743ec9b0ef6eaebf5c762b1177d60b69e90bcd53e6d022a3761`  
		Last Modified: Wed, 15 Sep 2021 18:48:32 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6865ddeca380112eb05cd73aa051b641679ee53c53c1518f8a65ec43413e19c`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976c7967156aea258deb3e7fb1ab43f6cf27ee679271fa8a7621ff731d753cee`  
		Last Modified: Wed, 15 Sep 2021 18:48:33 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.3.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4f38ae124d0efb2392c4746560aa4dbd6be7de79c98c0c6b01d3c1805f339176
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362066251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a6eea957e927ab8f3b6c59bc55b761506bf757df5c835b16557f6d8eb0ea27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:09:34 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:09:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:09:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:09:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:09:43 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:09:43 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:09:44 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:09:44 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:09:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:09:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:09:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Wed, 15 Sep 2021 18:09:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:09:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:09:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa3a82789006023c6b746e3f23a75b4c230873809340254f4785d1f77097725`  
		Last Modified: Wed, 15 Sep 2021 18:16:50 GMT  
		Size: 252.1 MB (252119353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da807595a8b2a47dc84f1a48745d5c5e9d0e96a4cacf0c5a362273519a1aa783`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 1.6 MB (1567819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77975723368b5d9b05b5c84ec3e477b3a32c817daa1c784c7c4ff81abf1f6ce7`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a66907876f27dad084e239771168e2c64543ae1b9ff1c144f363c4a87b980`  
		Last Modified: Wed, 15 Sep 2021 18:16:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e3c070a33a70c801d61edabf6ee388904fa1966f86c63ade12c0b778da5b2`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0687ec88c4740cb59d7cfb9d9705167478b75db03b896937fe38f6a6a815b5e5`  
		Last Modified: Wed, 15 Sep 2021 18:16:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.4`

```console
$ docker pull crate@sha256:c840dc91871cc84da834aa80df6d7a58a03295a99116c03a9f1b29f03916a9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.4` - linux; amd64

```console
$ docker pull crate@sha256:412e5813cba63e51619689c1089c80c037a3272f6d3e6db53cd33498770ad81f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333363835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1be805518776e61b40a7248adea924a45092b194df912fceda5ed117b8d3c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:41:05 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:41:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:41:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:41:10 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:41:10 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:41:11 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:41:11 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:41:11 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:41:11 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:41:11 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:41:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Wed, 15 Sep 2021 18:41:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:41:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c2d887a991063f39b2f8e8dc6c0668c828601e7c620da769aab3228c0eed2d`  
		Last Modified: Wed, 15 Sep 2021 18:48:14 GMT  
		Size: 255.7 MB (255680349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2268153cb1bd5bee6f52dccdc5b2fb5303b10e6c56de7a71b8db051694bc6723`  
		Last Modified: Wed, 15 Sep 2021 18:47:52 GMT  
		Size: 1.6 MB (1582191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4036b5434578ef285c4b74c2051ca386099a3f876e387f06211cdbdc8ee2fac`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a6d7f80099a1314911f9e3994de4e814a089a0d2170c20267d50d5ad0533ed`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d1a91b4f2fe26475fdc5c4fac140c791515aaaea3b8ac167bed23e84c5daa4`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6d0dae8952ee2e051d6662519edb9fca6d91e97f6a3dad2b0b8aae0ed3a0a4`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3c7615f6d76f94ffff4ef15b009f108b3c5fe05bbf2ee543e722db6dcb5f5e2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362399593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185317210434575f008d520a7c349b47f44be481a208d4bbb46a2bf0499b71a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:07:56 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:08:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:08:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:08:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:08:09 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:08:10 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:08:10 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:08:10 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:08:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:08:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:08:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Wed, 15 Sep 2021 18:08:11 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:08:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:08:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292ecf4d267cbb4ea24373d6e90a4cb484ffe86c080a761454c82b3330acae05`  
		Last Modified: Wed, 15 Sep 2021 18:16:08 GMT  
		Size: 252.4 MB (252438309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa64dc89280fa066189e0aa6dcb6b90379c40ee2cb230b99676d1ddd2a2fa1fa`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 1.6 MB (1582199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7862eefcbe4562b97d536c3de69673dea4e9896bf951017d47dd9e9523db3c2`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1d9a9781348f1e9c71776c842312a1d35ea4a1564c2a9b3229bc43b3cf3142`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63aa3d05007057ee0f7d4082441bf5c07147aff3d6b7be677da0eb33f928d520`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219413c1871066d971dacf6ce3fdfb75b238b35e7cf722d4c954a5824cc1f251`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.4.3`

```console
$ docker pull crate@sha256:c840dc91871cc84da834aa80df6d7a58a03295a99116c03a9f1b29f03916a9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.4.3` - linux; amd64

```console
$ docker pull crate@sha256:412e5813cba63e51619689c1089c80c037a3272f6d3e6db53cd33498770ad81f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333363835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1be805518776e61b40a7248adea924a45092b194df912fceda5ed117b8d3c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:41:05 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:41:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:41:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:41:10 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:41:10 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:41:11 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:41:11 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:41:11 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:41:11 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:41:11 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:41:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Wed, 15 Sep 2021 18:41:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:41:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c2d887a991063f39b2f8e8dc6c0668c828601e7c620da769aab3228c0eed2d`  
		Last Modified: Wed, 15 Sep 2021 18:48:14 GMT  
		Size: 255.7 MB (255680349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2268153cb1bd5bee6f52dccdc5b2fb5303b10e6c56de7a71b8db051694bc6723`  
		Last Modified: Wed, 15 Sep 2021 18:47:52 GMT  
		Size: 1.6 MB (1582191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4036b5434578ef285c4b74c2051ca386099a3f876e387f06211cdbdc8ee2fac`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a6d7f80099a1314911f9e3994de4e814a089a0d2170c20267d50d5ad0533ed`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d1a91b4f2fe26475fdc5c4fac140c791515aaaea3b8ac167bed23e84c5daa4`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6d0dae8952ee2e051d6662519edb9fca6d91e97f6a3dad2b0b8aae0ed3a0a4`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.4.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3c7615f6d76f94ffff4ef15b009f108b3c5fe05bbf2ee543e722db6dcb5f5e2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362399593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185317210434575f008d520a7c349b47f44be481a208d4bbb46a2bf0499b71a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:07:56 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:08:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:08:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:08:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:08:09 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:08:10 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:08:10 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:08:10 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:08:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:08:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:08:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Wed, 15 Sep 2021 18:08:11 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:08:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:08:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292ecf4d267cbb4ea24373d6e90a4cb484ffe86c080a761454c82b3330acae05`  
		Last Modified: Wed, 15 Sep 2021 18:16:08 GMT  
		Size: 252.4 MB (252438309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa64dc89280fa066189e0aa6dcb6b90379c40ee2cb230b99676d1ddd2a2fa1fa`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 1.6 MB (1582199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7862eefcbe4562b97d536c3de69673dea4e9896bf951017d47dd9e9523db3c2`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1d9a9781348f1e9c71776c842312a1d35ea4a1564c2a9b3229bc43b3cf3142`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63aa3d05007057ee0f7d4082441bf5c07147aff3d6b7be677da0eb33f928d520`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219413c1871066d971dacf6ce3fdfb75b238b35e7cf722d4c954a5824cc1f251`  
		Last Modified: Wed, 15 Sep 2021 18:15:40 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.5`

```console
$ docker pull crate@sha256:36d8fa7d7ccfbcd6a91d73b5e0fad480b199d7ff556936dcc7662e9fb9e16039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.5` - linux; amd64

```console
$ docker pull crate@sha256:3bdea75197f3a5f3c5f2318b28d1509603dc97d154f08d9ff49e007d59249751
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331650550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9310ed02fa2cc870131c0f01e1922b115040c5244f316d3a137427744d49ef0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:39:55 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.5.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.5.5.tar.gz.asc crate-4.5.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.5.5.tar.gz.asc     && tar -xf crate-4.5.5.tar.gz -C /crate --strip-components=1     && rm crate-4.5.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:40:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:40:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:40:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:40:08 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:40:08 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:40:08 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:40:08 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:40:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:40:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:40:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-07-20T11:42:19.930048 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.5.5
# Wed, 15 Sep 2021 18:40:09 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:40:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8877e6cec3d6e0ad0a8b734d1f0ff96af07a2cac6aa510cd60ec2d5764b30f7`  
		Last Modified: Wed, 15 Sep 2021 18:47:41 GMT  
		Size: 254.0 MB (253967058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cea4df4eec4b0d296dea3c2b0ff58110eaf490f833d52c23847550398a6da1c`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 1.6 MB (1582197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b005fffa42e7294136c8f7898c331ffe91e537d912381c3aaca37d3a02a2f2`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582efe38c9d11684ffb65600bb544c3f267d29dd84fc2e2522dba9d939adacaf`  
		Last Modified: Wed, 15 Sep 2021 18:47:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349bb2f74ff263c439e0675d3ef1ad9682c2b882d4fd3b2d44528be65a745e0e`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de10ea46dfdd51369dec0240f3a03ec10c0145418b4f783bbf672b8ec32de0`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bb8e9ca2f11435f6706edbf62e8245660354068758ea3de0dd36f0b4fe971107
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.7 MB (360687972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c3291a8fa6484cc36906a61c3517048eeab641da14f21d01b2440cc142e673`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Sat, 14 Nov 2020 00:40:26 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Sat, 14 Nov 2020 00:40:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:40:32 GMT
CMD ["/bin/bash"]
# Thu, 24 Jun 2021 18:41:15 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 19 Jul 2021 18:52:26 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.5.4.tar.gz.asc crate-4.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.5.4.tar.gz.asc     && tar -xf crate-4.5.4.tar.gz -C /crate --strip-components=1     && rm crate-4.5.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 19 Jul 2021 18:52:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 19 Jul 2021 18:52:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jul 2021 18:52:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 19 Jul 2021 18:52:36 GMT
RUN mkdir -p /data/data /data/log
# Mon, 19 Jul 2021 18:52:36 GMT
VOLUME [/data]
# Mon, 19 Jul 2021 18:52:37 GMT
WORKDIR /data
# Mon, 19 Jul 2021 18:52:37 GMT
EXPOSE 4200 4300 5432
# Mon, 19 Jul 2021 18:52:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 19 Jul 2021 18:52:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 19 Jul 2021 18:52:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-07-13T10:39:35.065268 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.5.4
# Mon, 19 Jul 2021 18:52:38 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 19 Jul 2021 18:52:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Jul 2021 18:52:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0504bae3036b8b424fe4a0fb15ad01fd1048486db6c038a1e8ba073fb637bf`  
		Last Modified: Thu, 24 Jun 2021 18:50:44 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f14e581eb6050eb5c4505c5b0d80307e71c19bda78a2568614a812739eeb74`  
		Last Modified: Mon, 19 Jul 2021 18:54:13 GMT  
		Size: 250.7 MB (250726694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5db7b36696f7346415162a2ced577f6c4521d22931b180627cd4d7513397707`  
		Last Modified: Mon, 19 Jul 2021 18:53:44 GMT  
		Size: 1.6 MB (1582188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3020f514bd0a240ec9c03386b50555e2c08239940a896ad6af81cf9afe2c944`  
		Last Modified: Mon, 19 Jul 2021 18:53:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab5368f393b3d5ccc8b6d61c2d2167a37c6a1cb4e75f57be2cae4058a3c9a0b`  
		Last Modified: Mon, 19 Jul 2021 18:53:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c09b7199b8ec9612a154658b07990209b646451da487b55237cdcb07fe1588`  
		Last Modified: Mon, 19 Jul 2021 18:53:44 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c297cc0f36d8d153006589c3c07f11e6448c7b912f1dcfe14f2a460d98014105`  
		Last Modified: Mon, 19 Jul 2021 18:53:44 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.5.5`

```console
$ docker pull crate@sha256:93b8869453f1b8eaf4f8962d67ebd399e6a7a8c00d5a953e3778b0577d72ff3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `crate:4.5.5` - linux; amd64

```console
$ docker pull crate@sha256:3bdea75197f3a5f3c5f2318b28d1509603dc97d154f08d9ff49e007d59249751
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331650550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9310ed02fa2cc870131c0f01e1922b115040c5244f316d3a137427744d49ef0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 15 Sep 2021 18:39:55 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.5.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.5.5.tar.gz.asc crate-4.5.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.5.5.tar.gz.asc     && tar -xf crate-4.5.5.tar.gz -C /crate --strip-components=1     && rm crate-4.5.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:40:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:40:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:40:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:40:08 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:40:08 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:40:08 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:40:08 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:40:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:40:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:40:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-07-20T11:42:19.930048 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.5.5
# Wed, 15 Sep 2021 18:40:09 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:40:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8877e6cec3d6e0ad0a8b734d1f0ff96af07a2cac6aa510cd60ec2d5764b30f7`  
		Last Modified: Wed, 15 Sep 2021 18:47:41 GMT  
		Size: 254.0 MB (253967058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cea4df4eec4b0d296dea3c2b0ff58110eaf490f833d52c23847550398a6da1c`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 1.6 MB (1582197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b005fffa42e7294136c8f7898c331ffe91e537d912381c3aaca37d3a02a2f2`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582efe38c9d11684ffb65600bb544c3f267d29dd84fc2e2522dba9d939adacaf`  
		Last Modified: Wed, 15 Sep 2021 18:47:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349bb2f74ff263c439e0675d3ef1ad9682c2b882d4fd3b2d44528be65a745e0e`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de10ea46dfdd51369dec0240f3a03ec10c0145418b4f783bbf672b8ec32de0`  
		Last Modified: Wed, 15 Sep 2021 18:47:03 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.6`

```console
$ docker pull crate@sha256:6037307285a47571edb1d52c4684488c5ee71723a494745e1a340d0ec3c0a20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6` - linux; amd64

```console
$ docker pull crate@sha256:9ada59f61dbd3a04baa6be96bb0e5523fee2a7d6ee158223feb203b4631dfeee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332885273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879339ea06ecc83e9df41ca6dcacea0086ff248c4ba77a657bad24570bdae843`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:22:22 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:22:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:22:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:22:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:22:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:22:29 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:22:29 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:22:30 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:22:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:22:30 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:22:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:22:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a005fb0a10da8a793f14f6d255fbc0523a581c642c527994e881af63cf5952c9`  
		Last Modified: Tue, 05 Oct 2021 22:23:37 GMT  
		Size: 255.2 MB (255201778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60be56f4c6c2c38c0c8ecf2f5f109577b5c94b2986e5fcf35a2caefab310f37c`  
		Last Modified: Tue, 05 Oct 2021 22:23:15 GMT  
		Size: 1.6 MB (1582196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2231b661e7b9b5e12f7fee501b02e503e16dd1ffd4541999fa1b3b7c0ecdf03a`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a020cfc7e3a4ea0ee5222d11046ee05ad33c9c9852f9a26c7277490fa47f9`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5841c0d2246c632837ec6ea295df94e0d74c0da602ddc26cbab74663cedc328d`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa95e2d2ee6a5b0b99546a53f3e2af785ae31693be72398481aa0bef2bdb00`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:76398e5ec8661eb1d809a31dfd3728ffebf48d4b5d8c16eecc33175181797c16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361950546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb4f1c16ee8b5fa0df0c1efb2a45c6864f311e68dbf46b103896dfdd0a165f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:42:33 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:42:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:42:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:42:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:42:48 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:42:48 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:42:48 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:42:49 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:42:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:42:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:42:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:42:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60520358f86a6d9fa0f0ec3cb6cdb07a56d948a288c48a579b7c84e945e04af2`  
		Last Modified: Tue, 05 Oct 2021 22:48:23 GMT  
		Size: 252.0 MB (251989270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bba2862655723cf05165c816f4665c52f3b2e9eadc31ff23f2f6b2136b4c0a`  
		Last Modified: Tue, 05 Oct 2021 22:47:56 GMT  
		Size: 1.6 MB (1582188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecf5ed3503cd74b35038b0395ea63386b136a6a4c6d1d70b953b01baf03bbb4`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9799643010467d3de3bd93930aa0347cf4b5903061bdbcfefb8530d195b2d9b7`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe435123f7a61476250dc2d81426731b63239a1b739c4b87891e09536121056`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956140fa2388d1557babd620ff2a416bd29296fa446f52199b436201abf1c62`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.6.4`

```console
$ docker pull crate@sha256:6037307285a47571edb1d52c4684488c5ee71723a494745e1a340d0ec3c0a20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6.4` - linux; amd64

```console
$ docker pull crate@sha256:9ada59f61dbd3a04baa6be96bb0e5523fee2a7d6ee158223feb203b4631dfeee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332885273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879339ea06ecc83e9df41ca6dcacea0086ff248c4ba77a657bad24570bdae843`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:22:22 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:22:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:22:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:22:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:22:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:22:29 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:22:29 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:22:30 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:22:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:22:30 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:22:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:22:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a005fb0a10da8a793f14f6d255fbc0523a581c642c527994e881af63cf5952c9`  
		Last Modified: Tue, 05 Oct 2021 22:23:37 GMT  
		Size: 255.2 MB (255201778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60be56f4c6c2c38c0c8ecf2f5f109577b5c94b2986e5fcf35a2caefab310f37c`  
		Last Modified: Tue, 05 Oct 2021 22:23:15 GMT  
		Size: 1.6 MB (1582196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2231b661e7b9b5e12f7fee501b02e503e16dd1ffd4541999fa1b3b7c0ecdf03a`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a020cfc7e3a4ea0ee5222d11046ee05ad33c9c9852f9a26c7277490fa47f9`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5841c0d2246c632837ec6ea295df94e0d74c0da602ddc26cbab74663cedc328d`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa95e2d2ee6a5b0b99546a53f3e2af785ae31693be72398481aa0bef2bdb00`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:76398e5ec8661eb1d809a31dfd3728ffebf48d4b5d8c16eecc33175181797c16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361950546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb4f1c16ee8b5fa0df0c1efb2a45c6864f311e68dbf46b103896dfdd0a165f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:42:33 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:42:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:42:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:42:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:42:48 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:42:48 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:42:48 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:42:49 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:42:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:42:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:42:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:42:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60520358f86a6d9fa0f0ec3cb6cdb07a56d948a288c48a579b7c84e945e04af2`  
		Last Modified: Tue, 05 Oct 2021 22:48:23 GMT  
		Size: 252.0 MB (251989270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bba2862655723cf05165c816f4665c52f3b2e9eadc31ff23f2f6b2136b4c0a`  
		Last Modified: Tue, 05 Oct 2021 22:47:56 GMT  
		Size: 1.6 MB (1582188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecf5ed3503cd74b35038b0395ea63386b136a6a4c6d1d70b953b01baf03bbb4`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9799643010467d3de3bd93930aa0347cf4b5903061bdbcfefb8530d195b2d9b7`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe435123f7a61476250dc2d81426731b63239a1b739c4b87891e09536121056`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956140fa2388d1557babd620ff2a416bd29296fa446f52199b436201abf1c62`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:6037307285a47571edb1d52c4684488c5ee71723a494745e1a340d0ec3c0a20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9ada59f61dbd3a04baa6be96bb0e5523fee2a7d6ee158223feb203b4631dfeee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332885273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879339ea06ecc83e9df41ca6dcacea0086ff248c4ba77a657bad24570bdae843`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:22:22 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:22:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:22:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:22:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:22:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:22:29 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:22:29 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:22:30 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:22:30 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:22:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:22:30 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:22:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:22:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a005fb0a10da8a793f14f6d255fbc0523a581c642c527994e881af63cf5952c9`  
		Last Modified: Tue, 05 Oct 2021 22:23:37 GMT  
		Size: 255.2 MB (255201778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60be56f4c6c2c38c0c8ecf2f5f109577b5c94b2986e5fcf35a2caefab310f37c`  
		Last Modified: Tue, 05 Oct 2021 22:23:15 GMT  
		Size: 1.6 MB (1582196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2231b661e7b9b5e12f7fee501b02e503e16dd1ffd4541999fa1b3b7c0ecdf03a`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a020cfc7e3a4ea0ee5222d11046ee05ad33c9c9852f9a26c7277490fa47f9`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5841c0d2246c632837ec6ea295df94e0d74c0da602ddc26cbab74663cedc328d`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa95e2d2ee6a5b0b99546a53f3e2af785ae31693be72398481aa0bef2bdb00`  
		Last Modified: Tue, 05 Oct 2021 22:23:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:76398e5ec8661eb1d809a31dfd3728ffebf48d4b5d8c16eecc33175181797c16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361950546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb4f1c16ee8b5fa0df0c1efb2a45c6864f311e68dbf46b103896dfdd0a165f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:03:27 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 05 Oct 2021 22:42:33 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.4.tar.gz.asc crate-4.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.4.tar.gz.asc     && tar -xf crate-4.6.4.tar.gz -C /crate --strip-components=1     && rm crate-4.6.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 05 Oct 2021 22:42:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Oct 2021 22:42:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 22:42:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Oct 2021 22:42:48 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Oct 2021 22:42:48 GMT
VOLUME [/data]
# Tue, 05 Oct 2021 22:42:48 GMT
WORKDIR /data
# Tue, 05 Oct 2021 22:42:49 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Oct 2021 22:42:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Oct 2021 22:42:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-30T17:09:13.685861 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.4
# Tue, 05 Oct 2021 22:42:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Oct 2021 22:42:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 22:42:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba2218bab9ebc3c118f07cc854153c5a0c3c9b251c26673a1c24bbfe59f44d`  
		Last Modified: Wed, 15 Sep 2021 18:14:59 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60520358f86a6d9fa0f0ec3cb6cdb07a56d948a288c48a579b7c84e945e04af2`  
		Last Modified: Tue, 05 Oct 2021 22:48:23 GMT  
		Size: 252.0 MB (251989270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bba2862655723cf05165c816f4665c52f3b2e9eadc31ff23f2f6b2136b4c0a`  
		Last Modified: Tue, 05 Oct 2021 22:47:56 GMT  
		Size: 1.6 MB (1582188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecf5ed3503cd74b35038b0395ea63386b136a6a4c6d1d70b953b01baf03bbb4`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9799643010467d3de3bd93930aa0347cf4b5903061bdbcfefb8530d195b2d9b7`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe435123f7a61476250dc2d81426731b63239a1b739c4b87891e09536121056`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956140fa2388d1557babd620ff2a416bd29296fa446f52199b436201abf1c62`  
		Last Modified: Tue, 05 Oct 2021 22:47:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
