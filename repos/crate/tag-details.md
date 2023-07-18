<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.8`](#crate48)
-	[`crate:4.8.4`](#crate484)
-	[`crate:5.3`](#crate53)
-	[`crate:5.3.4`](#crate534)
-	[`crate:5.4`](#crate54)
-	[`crate:5.4.0`](#crate540)
-	[`crate:latest`](#cratelatest)

## `crate:4.8`

```console
$ docker pull crate@sha256:fcfb1e26e4b6b84cf23bbb0de51a9671655d1e843b01cffea5984643727e021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8` - linux; amd64

```console
$ docker pull crate@sha256:ab33e064e23959eed997f0e9317a8ccb942974f7d3159ac464a5a3cb221e25c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366609762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849c866b7319b231f9f5482aef88650ec60dd6d7059a29de576cbd4b789bd3d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 19:20:47 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 20 Sep 2022 20:24:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Tue, 20 Sep 2022 20:24:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 20 Sep 2022 20:24:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Sep 2022 20:24:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 20 Sep 2022 20:24:33 GMT
RUN mkdir -p /data/data /data/log
# Tue, 20 Sep 2022 20:24:33 GMT
VOLUME [/data]
# Tue, 20 Sep 2022 20:24:33 GMT
WORKDIR /data
# Tue, 20 Sep 2022 20:24:33 GMT
EXPOSE 4200 4300 5432
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 20 Sep 2022 20:24:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Tue, 20 Sep 2022 20:24:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 20 Sep 2022 20:24:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Sep 2022 20:24:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816162095613648af0045121a146a6ab058718d006d17f2ea25e169f0961b298`  
		Last Modified: Mon, 12 Sep 2022 19:22:25 GMT  
		Size: 77.1 MB (77149352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3bdb3f3876f51c5600bc5d5576e6c84959f5433fb375eb3a1b2798d93abc31`  
		Last Modified: Tue, 20 Sep 2022 20:25:15 GMT  
		Size: 211.7 MB (211650590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d385fe2b73321323b7b11085d41441495146f7a18dbf421502225a9ff8656`  
		Last Modified: Tue, 20 Sep 2022 20:24:54 GMT  
		Size: 1.7 MB (1710779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c312f86d93dded0d735bc9b7234f64c5a8ff5bc82ffe1ce9ad869ed3a7b68c68`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaec4222433c7af8e5220f511915ab8fb4049a7136fc371b5d2679811e34c4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed829b350fc610813c498009ca8aecf3b3e6184dfe54943a7d490e583e207f4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2994a6708f131a2fa358dbb8885094c2d552f7880f924a3b84048082560032f3`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:54bb068652a7f229af18cc10ae7e5d94d19cbbf4952635694dc2e34df3502b56
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666503011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29f1818d2fdc8991ad2484f8adac7e43311743dae8b71f35d1eda47c45be02`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 24 Oct 2022 21:41:05 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 24 Oct 2022 21:42:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Mon, 24 Oct 2022 21:42:23 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Oct 2022 21:42:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 21:42:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Oct 2022 21:42:24 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Oct 2022 21:42:24 GMT
VOLUME [/data]
# Mon, 24 Oct 2022 21:42:24 GMT
WORKDIR /data
# Mon, 24 Oct 2022 21:42:24 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Oct 2022 21:42:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Mon, 24 Oct 2022 21:42:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Oct 2022 21:42:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Oct 2022 21:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bd2dd4fe2ac3696c00e2e33054e11971bf81acb6591869e1d525feb18cceb3`  
		Last Modified: Mon, 24 Oct 2022 21:45:28 GMT  
		Size: 346.0 MB (345996846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5e7c58b367faadd294e7b188398fc564edf19271fac04a26b51637c28e43e6`  
		Last Modified: Mon, 24 Oct 2022 21:45:57 GMT  
		Size: 210.4 MB (210418568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b966a9d970d836ffb3ccc8dcca4ffd79e2f6334cb230e0617b25457394750b`  
		Last Modified: Mon, 24 Oct 2022 21:45:42 GMT  
		Size: 1.7 MB (1710769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286650217f63a621366b0d7e1115fa37df60654f36c5b556c3b2a5cf41e7f6cd`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d1e66c86b54db4e4dc22fce8f33097dcad2745154e050210dacb713db2c232`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a335f20bda4ea63d2b38a9c41ea60713b51e8b3816061c4067b7f69604ecf5f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293324d5cf1d0be9fc09670f9ab9249b7775dfb2a0c350042d4909228b55011f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8.4`

```console
$ docker pull crate@sha256:fcfb1e26e4b6b84cf23bbb0de51a9671655d1e843b01cffea5984643727e021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8.4` - linux; amd64

```console
$ docker pull crate@sha256:ab33e064e23959eed997f0e9317a8ccb942974f7d3159ac464a5a3cb221e25c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366609762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849c866b7319b231f9f5482aef88650ec60dd6d7059a29de576cbd4b789bd3d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 19:20:47 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 20 Sep 2022 20:24:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Tue, 20 Sep 2022 20:24:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 20 Sep 2022 20:24:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Sep 2022 20:24:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 20 Sep 2022 20:24:33 GMT
RUN mkdir -p /data/data /data/log
# Tue, 20 Sep 2022 20:24:33 GMT
VOLUME [/data]
# Tue, 20 Sep 2022 20:24:33 GMT
WORKDIR /data
# Tue, 20 Sep 2022 20:24:33 GMT
EXPOSE 4200 4300 5432
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 20 Sep 2022 20:24:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Tue, 20 Sep 2022 20:24:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 20 Sep 2022 20:24:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Sep 2022 20:24:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816162095613648af0045121a146a6ab058718d006d17f2ea25e169f0961b298`  
		Last Modified: Mon, 12 Sep 2022 19:22:25 GMT  
		Size: 77.1 MB (77149352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3bdb3f3876f51c5600bc5d5576e6c84959f5433fb375eb3a1b2798d93abc31`  
		Last Modified: Tue, 20 Sep 2022 20:25:15 GMT  
		Size: 211.7 MB (211650590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d385fe2b73321323b7b11085d41441495146f7a18dbf421502225a9ff8656`  
		Last Modified: Tue, 20 Sep 2022 20:24:54 GMT  
		Size: 1.7 MB (1710779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c312f86d93dded0d735bc9b7234f64c5a8ff5bc82ffe1ce9ad869ed3a7b68c68`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaec4222433c7af8e5220f511915ab8fb4049a7136fc371b5d2679811e34c4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed829b350fc610813c498009ca8aecf3b3e6184dfe54943a7d490e583e207f4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2994a6708f131a2fa358dbb8885094c2d552f7880f924a3b84048082560032f3`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:54bb068652a7f229af18cc10ae7e5d94d19cbbf4952635694dc2e34df3502b56
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666503011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29f1818d2fdc8991ad2484f8adac7e43311743dae8b71f35d1eda47c45be02`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 24 Oct 2022 21:41:05 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 24 Oct 2022 21:42:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Mon, 24 Oct 2022 21:42:23 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Oct 2022 21:42:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 21:42:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Oct 2022 21:42:24 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Oct 2022 21:42:24 GMT
VOLUME [/data]
# Mon, 24 Oct 2022 21:42:24 GMT
WORKDIR /data
# Mon, 24 Oct 2022 21:42:24 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Oct 2022 21:42:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Mon, 24 Oct 2022 21:42:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Oct 2022 21:42:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Oct 2022 21:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bd2dd4fe2ac3696c00e2e33054e11971bf81acb6591869e1d525feb18cceb3`  
		Last Modified: Mon, 24 Oct 2022 21:45:28 GMT  
		Size: 346.0 MB (345996846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5e7c58b367faadd294e7b188398fc564edf19271fac04a26b51637c28e43e6`  
		Last Modified: Mon, 24 Oct 2022 21:45:57 GMT  
		Size: 210.4 MB (210418568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b966a9d970d836ffb3ccc8dcca4ffd79e2f6334cb230e0617b25457394750b`  
		Last Modified: Mon, 24 Oct 2022 21:45:42 GMT  
		Size: 1.7 MB (1710769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286650217f63a621366b0d7e1115fa37df60654f36c5b556c3b2a5cf41e7f6cd`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d1e66c86b54db4e4dc22fce8f33097dcad2745154e050210dacb713db2c232`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a335f20bda4ea63d2b38a9c41ea60713b51e8b3816061c4067b7f69604ecf5f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293324d5cf1d0be9fc09670f9ab9249b7775dfb2a0c350042d4909228b55011f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:8ccae387bf33ed9d327eb054c27a68763e1335f4068970356302dd3e6da36df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:e44a219fbb05a099cc86784041c5dda6c388830109c94d9679712582f8046821
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297834175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34174fb668e24a3eb11d51152bbc0a6e14de892a08f3b330c8391d8befdba024`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:27:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.4.tar.gz.asc crate-5.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.4.tar.gz.asc     && tar -xf crate-5.3.4.tar.gz -C /crate --strip-components=1     && rm crate-5.3.4.tar.gz
# Tue, 18 Jul 2023 19:27:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:27:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:27:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:27:23 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:27:23 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:27:23 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:27:23 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:27:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:27:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:27:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T09:48:31.716932 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.4
# Tue, 18 Jul 2023 19:27:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:27:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:27:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba0683db538369284e24c7054438f354fdeb76d5276c5b899e7d6aaf76446a`  
		Last Modified: Tue, 18 Jul 2023 19:28:24 GMT  
		Size: 227.3 MB (227335281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f46bc1d3d340849fc274b682c5fb0c354ffc694303ca7a9defe2c485126502`  
		Last Modified: Tue, 18 Jul 2023 19:28:07 GMT  
		Size: 1.9 MB (1857121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41daeee47ada5bd000e7c74b65cdc0537765a86b466098889417fd94695dd963`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dcc8e334da24a72df5700d3b2f8139c7c4187d4428d6df4a06ec12f2e95135`  
		Last Modified: Tue, 18 Jul 2023 19:28:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ed1fc38af6ed96f26149be3359096cc26f6ddaf786128f2f63ef3c54e2eeb1`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfbe3100b5e5ee904e23f5f284fe6f3270381eb804737bca8946dac2327ad02`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d5257888aca3e94af575237d5549de3e8761e9ad1d7aa6964a862933dca76384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295484096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d32df418c19f392b14ea1b93a976e5103ce035f6b5d98af7fc123993c8d3b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:45:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.4.tar.gz.asc crate-5.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.4.tar.gz.asc     && tar -xf crate-5.3.4.tar.gz -C /crate --strip-components=1     && rm crate-5.3.4.tar.gz
# Tue, 18 Jul 2023 19:45:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:45:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:45:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:45:09 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:45:09 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:45:09 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:45:09 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:45:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:45:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:45:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T09:48:31.716932 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.4
# Tue, 18 Jul 2023 19:45:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:45:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:45:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b860c111459f3c3af99f5a923509fd7a16991bb3e960829dda29805102394f1c`  
		Last Modified: Tue, 18 Jul 2023 19:46:02 GMT  
		Size: 226.1 MB (226074679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f214b776b813f143cc6ffee6c1587e889594caed51a2f10b432c22888db0853`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b1fedcac2e10f952586b71314dc1e61ffd75ea2e0785ed30669b71ff3eba77`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91138646825daf864af44b9197b608a85aa9212ea7a1571d217df7fe8c89fbfd`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96b96a459225e913cc3e765578ff438aacc88e0b1ebd87a34b7a2487240a169`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db2cf39edf1d22402e68d4c494c94ec16e73c3eb262f6875eac586f14c6b62`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.4`

```console
$ docker pull crate@sha256:8ccae387bf33ed9d327eb054c27a68763e1335f4068970356302dd3e6da36df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.4` - linux; amd64

```console
$ docker pull crate@sha256:e44a219fbb05a099cc86784041c5dda6c388830109c94d9679712582f8046821
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297834175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34174fb668e24a3eb11d51152bbc0a6e14de892a08f3b330c8391d8befdba024`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:27:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.4.tar.gz.asc crate-5.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.4.tar.gz.asc     && tar -xf crate-5.3.4.tar.gz -C /crate --strip-components=1     && rm crate-5.3.4.tar.gz
# Tue, 18 Jul 2023 19:27:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:27:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:27:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:27:23 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:27:23 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:27:23 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:27:23 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:27:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:27:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:27:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T09:48:31.716932 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.4
# Tue, 18 Jul 2023 19:27:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:27:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:27:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba0683db538369284e24c7054438f354fdeb76d5276c5b899e7d6aaf76446a`  
		Last Modified: Tue, 18 Jul 2023 19:28:24 GMT  
		Size: 227.3 MB (227335281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f46bc1d3d340849fc274b682c5fb0c354ffc694303ca7a9defe2c485126502`  
		Last Modified: Tue, 18 Jul 2023 19:28:07 GMT  
		Size: 1.9 MB (1857121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41daeee47ada5bd000e7c74b65cdc0537765a86b466098889417fd94695dd963`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dcc8e334da24a72df5700d3b2f8139c7c4187d4428d6df4a06ec12f2e95135`  
		Last Modified: Tue, 18 Jul 2023 19:28:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ed1fc38af6ed96f26149be3359096cc26f6ddaf786128f2f63ef3c54e2eeb1`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfbe3100b5e5ee904e23f5f284fe6f3270381eb804737bca8946dac2327ad02`  
		Last Modified: Tue, 18 Jul 2023 19:28:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d5257888aca3e94af575237d5549de3e8761e9ad1d7aa6964a862933dca76384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295484096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d32df418c19f392b14ea1b93a976e5103ce035f6b5d98af7fc123993c8d3b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:45:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.4.tar.gz.asc crate-5.3.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.4.tar.gz.asc     && tar -xf crate-5.3.4.tar.gz -C /crate --strip-components=1     && rm crate-5.3.4.tar.gz
# Tue, 18 Jul 2023 19:45:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:45:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:45:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:45:09 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:45:09 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:45:09 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:45:09 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:45:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:45:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:45:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T09:48:31.716932 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.4
# Tue, 18 Jul 2023 19:45:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:45:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:45:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b860c111459f3c3af99f5a923509fd7a16991bb3e960829dda29805102394f1c`  
		Last Modified: Tue, 18 Jul 2023 19:46:02 GMT  
		Size: 226.1 MB (226074679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f214b776b813f143cc6ffee6c1587e889594caed51a2f10b432c22888db0853`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b1fedcac2e10f952586b71314dc1e61ffd75ea2e0785ed30669b71ff3eba77`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91138646825daf864af44b9197b608a85aa9212ea7a1571d217df7fe8c89fbfd`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96b96a459225e913cc3e765578ff438aacc88e0b1ebd87a34b7a2487240a169`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db2cf39edf1d22402e68d4c494c94ec16e73c3eb262f6875eac586f14c6b62`  
		Last Modified: Tue, 18 Jul 2023 19:45:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:fd16537709d4ddc6d2477999ec3e62785d49714c917876eac942f1d575d76ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:e0d4082d41a795a60c9fc52a0ac3adbbaec99670d4311d4a5799d3b2765695cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299696004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb7652c7e23cdcfa7aafb88ff2c19cd01cddf9c5da4328c77fd1fbc62cb6c1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:26:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:27:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:27:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:27:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:27:02 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:27:02 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:27:03 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:27:03 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:27:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:27:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:27:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:27:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15ab74912a9625f62775fcdc2468ac28425352f0eaaa01be047bda36a74a821`  
		Last Modified: Tue, 18 Jul 2023 19:27:54 GMT  
		Size: 229.1 MB (229122505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db994ac1bca3c28f63b30fbb81c1bae66fe881c3529e112bfaad8e9452909bfa`  
		Last Modified: Tue, 18 Jul 2023 19:27:37 GMT  
		Size: 1.9 MB (1931723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44582da7d4cf7276bd13b03a7f449c555f1cbd2b3a437595e6fb3a4dfdde4d0e`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac99c355b0229b28de9d511dd8b4755e5099755aa8e3e6e6f1bd126d280e83`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca353b4b9ec3a91400eaa835c1d5c22e999b1d5ec35f47b02d3e128e648fb78`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c132fe158dfb7086af0b5547acfbe7257c51184cb42e6ad998294cd45f195982`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:65b9ac4b3a0d207b02d5e740a3e2b8f6138ac0d9825c2abad3d55a0472519b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296971190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5174c85ee03645eabe455fc82afa3eca6808840cf2b3de11186fa9a177999097`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:44:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:44:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:44:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:44:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:44:47 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:44:47 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:44:47 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:44:47 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:44:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:44:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:44:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:44:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:44:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6b734475509b94153ee7e1ab77662defc3c88c7371e6ecaef15c34a4fd5ca`  
		Last Modified: Tue, 18 Jul 2023 19:45:35 GMT  
		Size: 227.5 MB (227487178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a874f261b65ceb539944b7d9cea229d951e090f86176270bfb91e1942dddbb`  
		Last Modified: Tue, 18 Jul 2023 19:45:21 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11da72393fd32209d352298f3d6d0ee9a4bf1ea1a871ca41ce91d7cd4d6f9b5`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e43485ffe2b5fc6050c40d061343b40c95541a9b12206ffbde34bca6c5735fc`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc9ff41967fadaba2589c577b2137dc0cce52a30f8d522b02f82feee088cb4e`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed54a190ed73e4b3655ba0382ba1cae4aae73035468849282d59ae5a2488679`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.0`

```console
$ docker pull crate@sha256:fd16537709d4ddc6d2477999ec3e62785d49714c917876eac942f1d575d76ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.0` - linux; amd64

```console
$ docker pull crate@sha256:e0d4082d41a795a60c9fc52a0ac3adbbaec99670d4311d4a5799d3b2765695cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299696004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb7652c7e23cdcfa7aafb88ff2c19cd01cddf9c5da4328c77fd1fbc62cb6c1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:26:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:27:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:27:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:27:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:27:02 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:27:02 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:27:03 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:27:03 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:27:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:27:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:27:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:27:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15ab74912a9625f62775fcdc2468ac28425352f0eaaa01be047bda36a74a821`  
		Last Modified: Tue, 18 Jul 2023 19:27:54 GMT  
		Size: 229.1 MB (229122505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db994ac1bca3c28f63b30fbb81c1bae66fe881c3529e112bfaad8e9452909bfa`  
		Last Modified: Tue, 18 Jul 2023 19:27:37 GMT  
		Size: 1.9 MB (1931723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44582da7d4cf7276bd13b03a7f449c555f1cbd2b3a437595e6fb3a4dfdde4d0e`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac99c355b0229b28de9d511dd8b4755e5099755aa8e3e6e6f1bd126d280e83`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca353b4b9ec3a91400eaa835c1d5c22e999b1d5ec35f47b02d3e128e648fb78`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c132fe158dfb7086af0b5547acfbe7257c51184cb42e6ad998294cd45f195982`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:65b9ac4b3a0d207b02d5e740a3e2b8f6138ac0d9825c2abad3d55a0472519b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296971190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5174c85ee03645eabe455fc82afa3eca6808840cf2b3de11186fa9a177999097`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:44:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:44:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:44:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:44:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:44:47 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:44:47 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:44:47 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:44:47 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:44:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:44:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:44:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:44:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:44:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6b734475509b94153ee7e1ab77662defc3c88c7371e6ecaef15c34a4fd5ca`  
		Last Modified: Tue, 18 Jul 2023 19:45:35 GMT  
		Size: 227.5 MB (227487178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a874f261b65ceb539944b7d9cea229d951e090f86176270bfb91e1942dddbb`  
		Last Modified: Tue, 18 Jul 2023 19:45:21 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11da72393fd32209d352298f3d6d0ee9a4bf1ea1a871ca41ce91d7cd4d6f9b5`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e43485ffe2b5fc6050c40d061343b40c95541a9b12206ffbde34bca6c5735fc`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc9ff41967fadaba2589c577b2137dc0cce52a30f8d522b02f82feee088cb4e`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed54a190ed73e4b3655ba0382ba1cae4aae73035468849282d59ae5a2488679`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:fd16537709d4ddc6d2477999ec3e62785d49714c917876eac942f1d575d76ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e0d4082d41a795a60c9fc52a0ac3adbbaec99670d4311d4a5799d3b2765695cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299696004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb7652c7e23cdcfa7aafb88ff2c19cd01cddf9c5da4328c77fd1fbc62cb6c1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:26:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:27:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:27:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:27:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:27:02 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:27:02 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:27:03 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:27:03 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:27:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:27:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:27:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:27:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:27:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15ab74912a9625f62775fcdc2468ac28425352f0eaaa01be047bda36a74a821`  
		Last Modified: Tue, 18 Jul 2023 19:27:54 GMT  
		Size: 229.1 MB (229122505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db994ac1bca3c28f63b30fbb81c1bae66fe881c3529e112bfaad8e9452909bfa`  
		Last Modified: Tue, 18 Jul 2023 19:27:37 GMT  
		Size: 1.9 MB (1931723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44582da7d4cf7276bd13b03a7f449c555f1cbd2b3a437595e6fb3a4dfdde4d0e`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac99c355b0229b28de9d511dd8b4755e5099755aa8e3e6e6f1bd126d280e83`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca353b4b9ec3a91400eaa835c1d5c22e999b1d5ec35f47b02d3e128e648fb78`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c132fe158dfb7086af0b5547acfbe7257c51184cb42e6ad998294cd45f195982`  
		Last Modified: Tue, 18 Jul 2023 19:27:36 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:65b9ac4b3a0d207b02d5e740a3e2b8f6138ac0d9825c2abad3d55a0472519b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296971190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5174c85ee03645eabe455fc82afa3eca6808840cf2b3de11186fa9a177999097`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 18 Jul 2023 19:44:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.0.tar.gz.asc crate-5.4.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.0.tar.gz.asc     && tar -xf crate-5.4.0.tar.gz -C /crate --strip-components=1     && rm crate-5.4.0.tar.gz
# Tue, 18 Jul 2023 19:44:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Jul 2023 19:44:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jul 2023 19:44:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Jul 2023 19:44:47 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Jul 2023 19:44:47 GMT
VOLUME [/data]
# Tue, 18 Jul 2023 19:44:47 GMT
WORKDIR /data
# Tue, 18 Jul 2023 19:44:47 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Jul 2023 19:44:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Jul 2023 19:44:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Jul 2023 19:44:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-07-11T14:38:05.395912 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.0
# Tue, 18 Jul 2023 19:44:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 18 Jul 2023 19:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jul 2023 19:44:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6b734475509b94153ee7e1ab77662defc3c88c7371e6ecaef15c34a4fd5ca`  
		Last Modified: Tue, 18 Jul 2023 19:45:35 GMT  
		Size: 227.5 MB (227487178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a874f261b65ceb539944b7d9cea229d951e090f86176270bfb91e1942dddbb`  
		Last Modified: Tue, 18 Jul 2023 19:45:21 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11da72393fd32209d352298f3d6d0ee9a4bf1ea1a871ca41ce91d7cd4d6f9b5`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e43485ffe2b5fc6050c40d061343b40c95541a9b12206ffbde34bca6c5735fc`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc9ff41967fadaba2589c577b2137dc0cce52a30f8d522b02f82feee088cb4e`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed54a190ed73e4b3655ba0382ba1cae4aae73035468849282d59ae5a2488679`  
		Last Modified: Tue, 18 Jul 2023 19:45:20 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
