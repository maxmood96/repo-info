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
-	[`crate:4.6.6`](#crate466)
-	[`crate:latest`](#cratelatest)

## `crate:3.3`

```console
$ docker pull crate@sha256:ac8e5e8ebcdc89d5ebf7551094deb99ce2ffaa496bde7debc2804007aa67179b
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
$ docker pull crate@sha256:68eba8bda6a48f52c04cc3c043068c7f417ef10aee06a9e59b9c07bed0a234b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377484863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8949ada6e6b1bc3bd7956aaf905b83cfadc7ca3e36ae50c5e8abe7ac48480fad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:50:17 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:50:18 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Fri, 19 Nov 2021 17:50:19 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:51:10 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Fri, 19 Nov 2021 17:51:11 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:51:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:51:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:51:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:51:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:51:23 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:51:23 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:51:24 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:51:25 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:51:27 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:51:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:51:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Fri, 19 Nov 2021 17:51:30 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:51:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:51:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b473abeb8dddd2248cec1a84621c3b6619687798d0de3791c272e66b464e160`  
		Last Modified: Fri, 19 Nov 2021 17:57:41 GMT  
		Size: 188.1 MB (188101480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e27c30a08f34be0fab91366c7e3bda63b53cdc496cf915f6311c152c3139ad`  
		Last Modified: Fri, 19 Nov 2021 17:57:23 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33710d7f5d99d3ab0dcaae0e6d00c155e5f8060b036975c6660d1f0a4b6c85e0`  
		Last Modified: Fri, 19 Nov 2021 17:57:36 GMT  
		Size: 79.7 MB (79711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630f43226f688e1911e4e930c24f7b239fccc37e1c416b2d3b98376da3b1310b`  
		Last Modified: Fri, 19 Nov 2021 17:57:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fda89b34864732cdfacd0b8f23cc3768d331f0cd73a7835db86f7b5e14f1c4`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d924d6898abf245ca7deda4bcec423cc24a5d9b397782fa249d5bc305946ae2`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 1.3 MB (1292746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006e4ec1cf9c08ac4bd86a59bd194f23fd2adfdf7dd51a47fa384ca52ce3fc1`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024010afc33fd51c30772323d306bf24e74cd8d1ae4302d4fc9757f9dd62d758`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:3.3.5`

```console
$ docker pull crate@sha256:ac8e5e8ebcdc89d5ebf7551094deb99ce2ffaa496bde7debc2804007aa67179b
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
$ docker pull crate@sha256:68eba8bda6a48f52c04cc3c043068c7f417ef10aee06a9e59b9c07bed0a234b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377484863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8949ada6e6b1bc3bd7956aaf905b83cfadc7ca3e36ae50c5e8abe7ac48480fad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:50:17 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz     && echo "7a6bb980b9c91c478421f865087ad2d69086a0583aeeb9e69204785e8e97dcfd */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:50:18 GMT
ENV JAVA_HOME=/opt/jdk-11.0.1
# Fri, 19 Nov 2021 17:50:19 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-11.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:51:10 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-3.3.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-3.3.5.tar.gz.asc crate-3.3.5.tar.gz     && rm -rf "$GNUPGHOME" crate-3.3.5.tar.gz.asc     && tar -xf crate-3.3.5.tar.gz -C /crate --strip-components=1     && rm crate-3.3.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Fri, 19 Nov 2021 17:51:11 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:51:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:51:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:51:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:51:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:51:23 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:51:23 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:51:24 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:51:25 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:51:27 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:51:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:51:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.label-schema.schema-version=1.0 org.label-schema.build-date=2020-08-20T09:47:47.048235 org.label-schema.name=crate org.label-schema.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.label-schema.url=https://crate.io/products/cratedb/ org.label-schema.vcs-url=https://github.com/crate/docker-crate org.label-schema.vendor=Crate.io org.label-schema.version=3.3.5
# Fri, 19 Nov 2021 17:51:30 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:51:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:51:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b473abeb8dddd2248cec1a84621c3b6619687798d0de3791c272e66b464e160`  
		Last Modified: Fri, 19 Nov 2021 17:57:41 GMT  
		Size: 188.1 MB (188101480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e27c30a08f34be0fab91366c7e3bda63b53cdc496cf915f6311c152c3139ad`  
		Last Modified: Fri, 19 Nov 2021 17:57:23 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33710d7f5d99d3ab0dcaae0e6d00c155e5f8060b036975c6660d1f0a4b6c85e0`  
		Last Modified: Fri, 19 Nov 2021 17:57:36 GMT  
		Size: 79.7 MB (79711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630f43226f688e1911e4e930c24f7b239fccc37e1c416b2d3b98376da3b1310b`  
		Last Modified: Fri, 19 Nov 2021 17:57:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fda89b34864732cdfacd0b8f23cc3768d331f0cd73a7835db86f7b5e14f1c4`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d924d6898abf245ca7deda4bcec423cc24a5d9b397782fa249d5bc305946ae2`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 1.3 MB (1292746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006e4ec1cf9c08ac4bd86a59bd194f23fd2adfdf7dd51a47fa384ca52ce3fc1`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024010afc33fd51c30772323d306bf24e74cd8d1ae4302d4fc9757f9dd62d758`  
		Last Modified: Fri, 19 Nov 2021 17:57:21 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0`

```console
$ docker pull crate@sha256:8eb24fe33d6a95b61c984d5f4744da903fe1067d72fef26f322916eac34b91b7
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
$ docker pull crate@sha256:5e7b4c2b20d48d198e6f4bf3004d2213f9bf3b9b6be18b91085f9484f9e426d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371403072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763f96561c0e9662cef8aab992201c7d0df7cfd4992bdfbf5367f8e5b4f9a1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:48:46 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:48:47 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Fri, 19 Nov 2021 17:48:48 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:49:34 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Fri, 19 Nov 2021 17:49:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:49:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:49:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:49:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:49:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:49:41 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:49:42 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:49:43 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:49:44 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:49:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:49:47 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:49:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Fri, 19 Nov 2021 17:49:49 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:49:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:49:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2e14150c8ddacfa1bcd5925bfe46e7fced21e6ceeb0a6feb64ffeb14fdf639`  
		Last Modified: Fri, 19 Nov 2021 17:57:10 GMT  
		Size: 198.1 MB (198128132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a737d77f5e17c2a94882c158d19544fd4016eea5af56b8897ecf5b419fccc170`  
		Last Modified: Fri, 19 Nov 2021 17:56:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1b5ea54fb0a4ed97923b973abae7392fbff963c9ea73d53eb1d72b18f92026`  
		Last Modified: Fri, 19 Nov 2021 17:56:57 GMT  
		Size: 63.6 MB (63602955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01cfaa76e5acff3339ccef110bca59bbd11ae9ee2438a3ec278d1a83836a27b`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac850efe035082a5e00ed7d635703f543dbded39fb7689db6c0be3e7ad3512e`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2568051bea186b6edf5f20448fbe513c39ca3c459b006c79b51b23dc5e00aa7`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 1.3 MB (1292750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e3f0f9014221c29e23554602dd95d6295cb123ecc1b70cb600533b12dc1c78`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7940c182f2ef2f6916ff0c7e77bb6b4275daea25b0d8f80416b11690533b90`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.0.12`

```console
$ docker pull crate@sha256:8eb24fe33d6a95b61c984d5f4744da903fe1067d72fef26f322916eac34b91b7
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
$ docker pull crate@sha256:5e7b4c2b20d48d198e6f4bf3004d2213f9bf3b9b6be18b91085f9484f9e426d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371403072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763f96561c0e9662cef8aab992201c7d0df7cfd4992bdfbf5367f8e5b4f9a1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:48:46 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk12.0.1/69cfe15208a647278a19ef0990eea691/12/GPL/openjdk-12.0.1_linux-x64_bin.tar.gz     && echo "151eb4ec00f82e5e951126f572dc9116104c884d97f91be14ec11e85fc2dd626 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:48:47 GMT
ENV JAVA_HOME=/opt/jdk-12.0.1
# Fri, 19 Nov 2021 17:48:48 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-12.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:49:34 GMT
RUN yum install -y yum-utils https://centos7.iuscommunity.org/ius-release.rpm     && yum makecache     && yum install -y python36u openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.0.12.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.0.12.tar.gz.asc crate-4.0.12.tar.gz     && rm -rf "$GNUPGHOME" crate-4.0.12.tar.gz.asc     && tar -xf crate-4.0.12.tar.gz -C /crate --strip-components=1     && rm crate-4.0.12.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Fri, 19 Nov 2021 17:49:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:49:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:49:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:49:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:49:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:49:41 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:49:42 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:49:43 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:49:44 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:49:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:49:47 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:49:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-01-30T15:00:47.948355 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.0.12
# Fri, 19 Nov 2021 17:49:49 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:49:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:49:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2e14150c8ddacfa1bcd5925bfe46e7fced21e6ceeb0a6feb64ffeb14fdf639`  
		Last Modified: Fri, 19 Nov 2021 17:57:10 GMT  
		Size: 198.1 MB (198128132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a737d77f5e17c2a94882c158d19544fd4016eea5af56b8897ecf5b419fccc170`  
		Last Modified: Fri, 19 Nov 2021 17:56:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1b5ea54fb0a4ed97923b973abae7392fbff963c9ea73d53eb1d72b18f92026`  
		Last Modified: Fri, 19 Nov 2021 17:56:57 GMT  
		Size: 63.6 MB (63602955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01cfaa76e5acff3339ccef110bca59bbd11ae9ee2438a3ec278d1a83836a27b`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac850efe035082a5e00ed7d635703f543dbded39fb7689db6c0be3e7ad3512e`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2568051bea186b6edf5f20448fbe513c39ca3c459b006c79b51b23dc5e00aa7`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 1.3 MB (1292750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e3f0f9014221c29e23554602dd95d6295cb123ecc1b70cb600533b12dc1c78`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7940c182f2ef2f6916ff0c7e77bb6b4275daea25b0d8f80416b11690533b90`  
		Last Modified: Fri, 19 Nov 2021 17:56:47 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.1`

```console
$ docker pull crate@sha256:5172dc27e6004ef1bcaca43c354e80ade6bd94068353e12cafd8c77db948ea18
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
$ docker pull crate@sha256:ad64cfce3772dedd0ca9a1d6c61e3191624de8e45ab8a080c7cb3da12fe08fd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 MB (384067590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb220339ea3c74b50c8270e24e97287b756c87f5d285a2764132518125bc0d3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:47:34 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:47:34 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Fri, 19 Nov 2021 17:47:35 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:48:08 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:48:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:48:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:48:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:48:15 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:48:16 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:48:17 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:48:18 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:48:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:48:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:48:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Fri, 19 Nov 2021 17:48:23 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:48:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:48:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8061e684eae0b54e8eff350aa2181f0379aea17e8b0c1b050e6d6ac96bc719d`  
		Last Modified: Fri, 19 Nov 2021 17:56:36 GMT  
		Size: 196.4 MB (196422986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f1a7abf10bd305aa6262d529c13dd068429506feb4dd1910050ffb40932935`  
		Last Modified: Fri, 19 Nov 2021 17:56:14 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e63c9dfec00bd1fee3f3a83c15ede98d4436538d93be81371f1260757625764`  
		Last Modified: Fri, 19 Nov 2021 17:56:22 GMT  
		Size: 78.0 MB (77972614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e38691a10ac8648c6d1389d2626fecf47cdc460813de1ffc81f73989bde8a9`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 1.3 MB (1292752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0666c1602e2419bc14a7bc73015604dbda2d3dd3ab65dc2c455f2bb220c1e92`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dd167e3af1884b8b4fd8d098bd6ba0d3b50d2e0fb9701d7bc9d6796d4d370e`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d885bcadff1401c6c2d02584c148de3784228847e69ca8f357dccaaf2ba379`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ca0114754c092c0d58024366c46c4babb9df17d0d3e91515df9479885591e`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.1.8`

```console
$ docker pull crate@sha256:5172dc27e6004ef1bcaca43c354e80ade6bd94068353e12cafd8c77db948ea18
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
$ docker pull crate@sha256:ad64cfce3772dedd0ca9a1d6c61e3191624de8e45ab8a080c7cb3da12fe08fd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 MB (384067590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb220339ea3c74b50c8270e24e97287b756c87f5d285a2764132518125bc0d3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:47:34 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Fri, 19 Nov 2021 17:47:34 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Fri, 19 Nov 2021 17:47:35 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Fri, 19 Nov 2021 17:48:08 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.8.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.8.tar.gz.asc crate-4.1.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.8.tar.gz.asc     && tar -xf crate-4.1.8.tar.gz -C /crate --strip-components=1     && rm crate-4.1.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:48:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:48:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:48:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:48:15 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:48:16 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:48:17 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:48:18 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:48:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:48:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:48:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-07T09:24:31.760994 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.8
# Fri, 19 Nov 2021 17:48:23 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Fri, 19 Nov 2021 17:48:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:48:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8061e684eae0b54e8eff350aa2181f0379aea17e8b0c1b050e6d6ac96bc719d`  
		Last Modified: Fri, 19 Nov 2021 17:56:36 GMT  
		Size: 196.4 MB (196422986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f1a7abf10bd305aa6262d529c13dd068429506feb4dd1910050ffb40932935`  
		Last Modified: Fri, 19 Nov 2021 17:56:14 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e63c9dfec00bd1fee3f3a83c15ede98d4436538d93be81371f1260757625764`  
		Last Modified: Fri, 19 Nov 2021 17:56:22 GMT  
		Size: 78.0 MB (77972614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e38691a10ac8648c6d1389d2626fecf47cdc460813de1ffc81f73989bde8a9`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 1.3 MB (1292752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0666c1602e2419bc14a7bc73015604dbda2d3dd3ab65dc2c455f2bb220c1e92`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dd167e3af1884b8b4fd8d098bd6ba0d3b50d2e0fb9701d7bc9d6796d4d370e`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d885bcadff1401c6c2d02584c148de3784228847e69ca8f357dccaaf2ba379`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ca0114754c092c0d58024366c46c4babb9df17d0d3e91515df9479885591e`  
		Last Modified: Fri, 19 Nov 2021 17:56:12 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.2`

```console
$ docker pull crate@sha256:f1226147cb14e42150fc011a72ba565dad885e744645f70a2d70f842fb42940a
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
$ docker pull crate@sha256:fb893a49ffecd26dbc2213dc9bdbc673f056a5156c42ea74e69994f263c7e107
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363221070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee158641fe238569768a211fa8dbb1f11ef8ebbcb905aea14791d96bc926fff0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:46:59 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:47:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:47:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:47:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:47:04 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:47:04 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:47:05 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:47:06 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:47:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:47:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:47:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Fri, 19 Nov 2021 17:47:11 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:47:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110e33c97c472f2b1e2118c6ef930fab7d4f486b439e5f3fa2a0fdb40f38a39d`  
		Last Modified: Fri, 19 Nov 2021 17:55:56 GMT  
		Size: 253.3 MB (253275889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47d1605d3ba385cea696246e641d2f1d5cfc3356c3e8e4329808727db7cc5b`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 1.6 MB (1566178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fec568f73b7b3599c9474b0bca7d7384c2bc4cd5ac7ef3dba896affbb9352c`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67873c0c1a015bc47f40763b3613fa3b0997d994f093b906568d94464974760d`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db644d15ac160332af3abe800f43f878c4957df02511a9a374fb65c1542b2d`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffba7434ccd1e0e1d23878bc67cf11e04e6656de0c9244c938961363a30958e`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.2.7`

```console
$ docker pull crate@sha256:f1226147cb14e42150fc011a72ba565dad885e744645f70a2d70f842fb42940a
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
$ docker pull crate@sha256:fb893a49ffecd26dbc2213dc9bdbc673f056a5156c42ea74e69994f263c7e107
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363221070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee158641fe238569768a211fa8dbb1f11ef8ebbcb905aea14791d96bc926fff0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:46:59 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.7.tar.gz.asc crate-4.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.7.tar.gz.asc     && tar -xf crate-4.2.7.tar.gz -C /crate --strip-components=1     && rm crate-4.2.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:47:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:47:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:47:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:47:04 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:47:04 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:47:05 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:47:06 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:47:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:47:09 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:47:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-10-15T20:03:26.122288 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.7
# Fri, 19 Nov 2021 17:47:11 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:47:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110e33c97c472f2b1e2118c6ef930fab7d4f486b439e5f3fa2a0fdb40f38a39d`  
		Last Modified: Fri, 19 Nov 2021 17:55:56 GMT  
		Size: 253.3 MB (253275889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47d1605d3ba385cea696246e641d2f1d5cfc3356c3e8e4329808727db7cc5b`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 1.6 MB (1566178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fec568f73b7b3599c9474b0bca7d7384c2bc4cd5ac7ef3dba896affbb9352c`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67873c0c1a015bc47f40763b3613fa3b0997d994f093b906568d94464974760d`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db644d15ac160332af3abe800f43f878c4957df02511a9a374fb65c1542b2d`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffba7434ccd1e0e1d23878bc67cf11e04e6656de0c9244c938961363a30958e`  
		Last Modified: Fri, 19 Nov 2021 17:54:17 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.3`

```console
$ docker pull crate@sha256:cdb58dc28078593a738790acbfee7d397239c82db9b299b61d1cb6042502c344
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
$ docker pull crate@sha256:2b554fa6966747a99a6d8acdb986e1a0a85d0526716d1810b91792784fafd72e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362068167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ccbc71caf1267ed29eb3264302d56f98ea042f8daa4eb9724dbfad4a86e415`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:45:39 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:45:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:45:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:45:53 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:45:53 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:45:54 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:45:55 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:45:57 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:45:58 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:45:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Fri, 19 Nov 2021 17:46:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:46:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:46:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101ac1478b7351dae4eb0ae41d7f2213c9e6e172323e75fd8a5108198879576`  
		Last Modified: Fri, 19 Nov 2021 17:54:05 GMT  
		Size: 252.1 MB (252122982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79af7f3575a0846d6f90f265064fbf6c104004d77fb546693cb83b6c5538fc5`  
		Last Modified: Fri, 19 Nov 2021 17:53:39 GMT  
		Size: 1.6 MB (1566182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e4c15784dad22123b50a60be4632535b95a99d6aac09f08959c1e08f115f8c`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662972bf516d590f5e1292f41fef6c6a2136f2a0c451ee73ccf8d2d35d0a79d`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901e48873e201bfbad0d8a0ae8a3878b025493e48e71fe705ca4584803103a3`  
		Last Modified: Fri, 19 Nov 2021 17:53:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a10870e9b61d6e61c20754bafff4054d6f6bef30e08590a390a971b34857b0`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.3.4`

```console
$ docker pull crate@sha256:cdb58dc28078593a738790acbfee7d397239c82db9b299b61d1cb6042502c344
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
$ docker pull crate@sha256:2b554fa6966747a99a6d8acdb986e1a0a85d0526716d1810b91792784fafd72e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362068167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ccbc71caf1267ed29eb3264302d56f98ea042f8daa4eb9724dbfad4a86e415`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:45:39 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.4.tar.gz.asc crate-4.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.4.tar.gz.asc     && tar -xf crate-4.3.4.tar.gz -C /crate --strip-components=1     && rm crate-4.3.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:45:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:45:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:45:53 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:45:53 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:45:54 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:45:55 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:45:57 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:45:58 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:45:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-19T14:19:50.388804 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.4
# Fri, 19 Nov 2021 17:46:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:46:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:46:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101ac1478b7351dae4eb0ae41d7f2213c9e6e172323e75fd8a5108198879576`  
		Last Modified: Fri, 19 Nov 2021 17:54:05 GMT  
		Size: 252.1 MB (252122982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79af7f3575a0846d6f90f265064fbf6c104004d77fb546693cb83b6c5538fc5`  
		Last Modified: Fri, 19 Nov 2021 17:53:39 GMT  
		Size: 1.6 MB (1566182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e4c15784dad22123b50a60be4632535b95a99d6aac09f08959c1e08f115f8c`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662972bf516d590f5e1292f41fef6c6a2136f2a0c451ee73ccf8d2d35d0a79d`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901e48873e201bfbad0d8a0ae8a3878b025493e48e71fe705ca4584803103a3`  
		Last Modified: Fri, 19 Nov 2021 17:53:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a10870e9b61d6e61c20754bafff4054d6f6bef30e08590a390a971b34857b0`  
		Last Modified: Fri, 19 Nov 2021 17:53:38 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.4`

```console
$ docker pull crate@sha256:d6d63b8cf482c9ec47a0d9cc21918fd1445aa0bc42ee25cce48eb815d2894998
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
$ docker pull crate@sha256:595b873d0755b851a141accec2820b06127984c3c2d67120ea7d083b204dc72a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362397554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79c705a079250cf6e9f2f4cf733249627b40d05e897b3608124f92f9db0702b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:44:05 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:44:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:44:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:44:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:44:11 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:44:11 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:44:12 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:44:13 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:44:15 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:44:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:44:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Fri, 19 Nov 2021 17:44:18 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:44:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0703c68fb87b086dc5d4d23e236cd570b0110272a7115a0ee203e38a76160`  
		Last Modified: Fri, 19 Nov 2021 17:53:26 GMT  
		Size: 252.4 MB (252437976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3c998f6c5c8ed680bbbac99a095b17af6b0540d0818af0f99d342a6de372e6`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 1.6 MB (1580577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655a220931bec5d5757db314975476a672a5c0b4478af36b379e0f2467fa619`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95093f0ac632c2cff6379c7ac9b8317b45ea70f4c1dccf0ab751aa7c61a96570`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de8d14fabeb2b44c3ef428b705e50f5ea6255a59d5f56d77a19582afb26b3f5`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e047451ef6205cae500493285a4391f625629430afd16e4dc58fdf798375674d`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.4.3`

```console
$ docker pull crate@sha256:d6d63b8cf482c9ec47a0d9cc21918fd1445aa0bc42ee25cce48eb815d2894998
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
$ docker pull crate@sha256:595b873d0755b851a141accec2820b06127984c3c2d67120ea7d083b204dc72a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362397554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79c705a079250cf6e9f2f4cf733249627b40d05e897b3608124f92f9db0702b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:44:05 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.4.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.4.3.tar.gz.asc crate-4.4.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.4.3.tar.gz.asc     && tar -xf crate-4.4.3.tar.gz -C /crate --strip-components=1     && rm crate-4.4.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:44:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:44:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:44:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:44:11 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:44:11 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:44:12 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:44:13 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:44:15 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:44:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:44:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-03-23T11:20:23.363006 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.4.3
# Fri, 19 Nov 2021 17:44:18 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:44:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0703c68fb87b086dc5d4d23e236cd570b0110272a7115a0ee203e38a76160`  
		Last Modified: Fri, 19 Nov 2021 17:53:26 GMT  
		Size: 252.4 MB (252437976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3c998f6c5c8ed680bbbac99a095b17af6b0540d0818af0f99d342a6de372e6`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 1.6 MB (1580577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655a220931bec5d5757db314975476a672a5c0b4478af36b379e0f2467fa619`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95093f0ac632c2cff6379c7ac9b8317b45ea70f4c1dccf0ab751aa7c61a96570`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de8d14fabeb2b44c3ef428b705e50f5ea6255a59d5f56d77a19582afb26b3f5`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e047451ef6205cae500493285a4391f625629430afd16e4dc58fdf798375674d`  
		Last Modified: Fri, 19 Nov 2021 17:52:56 GMT  
		Size: 504.0 B  
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
$ docker pull crate@sha256:48715972cbfd9080d7858d88f952020de1f1d2bdb06caf878fab0042ca5441a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6` - linux; amd64

```console
$ docker pull crate@sha256:f87c1f8c30c29337043f5f06a1631223c150ee881e7f97bf28a70b387a212ac0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333090849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8fb4db28f0cb5b1b08b3becd777b660ce0b2727222c8f0327dd74aba49e53c`
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
# Fri, 19 Nov 2021 18:20:26 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.5.tar.gz.asc crate-4.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.5.tar.gz.asc     && tar -xf crate-4.6.5.tar.gz -C /crate --strip-components=1     && rm crate-4.6.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 18:20:30 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 18:20:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 18:20:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 18:20:32 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 18:20:32 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 18:20:32 GMT
WORKDIR /data
# Fri, 19 Nov 2021 18:20:32 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 18:20:32 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 18:20:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 18:20:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-11-12T20:22:37.835383 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.5
# Fri, 19 Nov 2021 18:20:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 18:20:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 18:20:33 GMT
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
	-	`sha256:3759362c63287819ade9aeddb60cfb39ccd5aa294f467522a570fa7bf28dd7a9`  
		Last Modified: Fri, 19 Nov 2021 18:21:32 GMT  
		Size: 255.4 MB (255407358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6c0b4bd2a140e0361053f199cb3fb689d5a82682b3b8a34edf9068a3d919b0`  
		Last Modified: Fri, 19 Nov 2021 18:21:10 GMT  
		Size: 1.6 MB (1582193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda3900c6b97cefcd815f34e09eaac92387e5e66a180c65573db3694041e675b`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad57d7785e8d12b131333bf6d45b08c8860257874ee9dca6c06dfefe9d3a1a1`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbee1478f232ae9c6d9bbf23cc0c4c4c8dede24c3e6472867717a498f21a0591`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5c28b8455ca2e19ee81a2be643a1e2ece1fce1326c759bd6a1223715f70398`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a0bae0dc6c18f89f4f2da273b751664d866caafad57c70aedf8fcd1d15e01d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362138349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ead85d0c9fc83bb464d8d170001da8c60b4e7eef1d7094ff26d2de641010d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:40:43 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.5.tar.gz.asc crate-4.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.5.tar.gz.asc     && tar -xf crate-4.6.5.tar.gz -C /crate --strip-components=1     && rm crate-4.6.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:40:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:40:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:40:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:40:57 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:40:57 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:40:58 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:40:59 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:41:01 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:41:02 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:41:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-11-12T20:22:37.835383 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.5
# Fri, 19 Nov 2021 17:41:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:41:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:41:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e5964bacb03197109bbbf5b7165ee0729e8f581b6dc5b52bd459e2d384d475`  
		Last Modified: Fri, 19 Nov 2021 17:52:41 GMT  
		Size: 252.2 MB (252178770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d233991bccabba8bd00a41207d15c3ad09458cd378980de5fc35e75899079f4`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 1.6 MB (1580578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74afc6d53814ef93777accf47b5437a920bd79664e854418f87e92f3b004b974`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6594b1d62e0f061f460ddbd93f613128ab10e0b50f213f06abe497e4aa5638be`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e18f3b9dc68b6bc14e7f38d02db4f7d798aec73fb2aea21f0689c6a71d8fc`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49900fae540b1b77979aaefeb9e456538b6833803d8e102ec61b73b80f6cf13`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.6.6`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:48715972cbfd9080d7858d88f952020de1f1d2bdb06caf878fab0042ca5441a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f87c1f8c30c29337043f5f06a1631223c150ee881e7f97bf28a70b387a212ac0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333090849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8fb4db28f0cb5b1b08b3becd777b660ce0b2727222c8f0327dd74aba49e53c`
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
# Fri, 19 Nov 2021 18:20:26 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.5.tar.gz.asc crate-4.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.5.tar.gz.asc     && tar -xf crate-4.6.5.tar.gz -C /crate --strip-components=1     && rm crate-4.6.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 18:20:30 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 18:20:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 18:20:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 18:20:32 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 18:20:32 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 18:20:32 GMT
WORKDIR /data
# Fri, 19 Nov 2021 18:20:32 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 18:20:32 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 18:20:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 18:20:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-11-12T20:22:37.835383 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.5
# Fri, 19 Nov 2021 18:20:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 18:20:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 18:20:33 GMT
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
	-	`sha256:3759362c63287819ade9aeddb60cfb39ccd5aa294f467522a570fa7bf28dd7a9`  
		Last Modified: Fri, 19 Nov 2021 18:21:32 GMT  
		Size: 255.4 MB (255407358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6c0b4bd2a140e0361053f199cb3fb689d5a82682b3b8a34edf9068a3d919b0`  
		Last Modified: Fri, 19 Nov 2021 18:21:10 GMT  
		Size: 1.6 MB (1582193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda3900c6b97cefcd815f34e09eaac92387e5e66a180c65573db3694041e675b`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad57d7785e8d12b131333bf6d45b08c8860257874ee9dca6c06dfefe9d3a1a1`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbee1478f232ae9c6d9bbf23cc0c4c4c8dede24c3e6472867717a498f21a0591`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5c28b8455ca2e19ee81a2be643a1e2ece1fce1326c759bd6a1223715f70398`  
		Last Modified: Fri, 19 Nov 2021 18:21:09 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a0bae0dc6c18f89f4f2da273b751664d866caafad57c70aedf8fcd1d15e01d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362138349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ead85d0c9fc83bb464d8d170001da8c60b4e7eef1d7094ff26d2de641010d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Fri, 19 Nov 2021 17:40:43 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.5.tar.gz.asc crate-4.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.5.tar.gz.asc     && tar -xf crate-4.6.5.tar.gz -C /crate --strip-components=1     && rm crate-4.6.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Fri, 19 Nov 2021 17:40:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 19 Nov 2021 17:40:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 17:40:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 19 Nov 2021 17:40:57 GMT
RUN mkdir -p /data/data /data/log
# Fri, 19 Nov 2021 17:40:57 GMT
VOLUME [/data]
# Fri, 19 Nov 2021 17:40:58 GMT
WORKDIR /data
# Fri, 19 Nov 2021 17:40:59 GMT
EXPOSE 4200 4300 5432
# Fri, 19 Nov 2021 17:41:01 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 19 Nov 2021 17:41:02 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 19 Nov 2021 17:41:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-11-12T20:22:37.835383 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.5
# Fri, 19 Nov 2021 17:41:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 19 Nov 2021 17:41:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 17:41:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e5964bacb03197109bbbf5b7165ee0729e8f581b6dc5b52bd459e2d384d475`  
		Last Modified: Fri, 19 Nov 2021 17:52:41 GMT  
		Size: 252.2 MB (252178770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d233991bccabba8bd00a41207d15c3ad09458cd378980de5fc35e75899079f4`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 1.6 MB (1580578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74afc6d53814ef93777accf47b5437a920bd79664e854418f87e92f3b004b974`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6594b1d62e0f061f460ddbd93f613128ab10e0b50f213f06abe497e4aa5638be`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e18f3b9dc68b6bc14e7f38d02db4f7d798aec73fb2aea21f0689c6a71d8fc`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49900fae540b1b77979aaefeb9e456538b6833803d8e102ec61b73b80f6cf13`  
		Last Modified: Fri, 19 Nov 2021 17:52:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
