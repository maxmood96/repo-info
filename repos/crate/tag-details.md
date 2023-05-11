<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.8`](#crate48)
-	[`crate:4.8.4`](#crate484)
-	[`crate:5.2`](#crate52)
-	[`crate:5.2.8`](#crate528)
-	[`crate:5.3`](#crate53)
-	[`crate:5.3.1`](#crate531)
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

## `crate:5.2`

```console
$ docker pull crate@sha256:e6a6a9a0d6e61e54a3d117370782adc678a4c131aec82a6d2a25a0907cb81913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2` - linux; amd64

```console
$ docker pull crate@sha256:88936482b6005c1c54717aa3745961b22f8985d95362b0f47df7446edf9226f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305961319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b535b974f78397298c7c25c8df853301028dea402ec1b1ac0aacb87f126717`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:48 GMT
ADD file:9022dcd506469f7fa13db0072d1e4ed93f0ddf853bdd9ff02efc8d5a0345bb78 in / 
# Tue, 11 Apr 2023 19:19:49 GMT
CMD ["/bin/bash"]
# Tue, 11 Apr 2023 19:36:50 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 11 May 2023 19:19:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Thu, 11 May 2023 19:19:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 11 May 2023 19:19:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:19:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 May 2023 19:19:54 GMT
RUN mkdir -p /data/data /data/log
# Thu, 11 May 2023 19:19:54 GMT
VOLUME [/data]
# Thu, 11 May 2023 19:19:54 GMT
WORKDIR /data
# Thu, 11 May 2023 19:19:55 GMT
EXPOSE 4200 4300 5432
# Thu, 11 May 2023 19:19:55 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 11 May 2023 19:19:55 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 11 May 2023 19:19:55 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Thu, 11 May 2023 19:19:55 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 11 May 2023 19:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 May 2023 19:19:55 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:349bb8f337e406f9e6bd67c41b36a6481834ff3cf177d4eaa707dd54d730be7b`  
		Last Modified: Tue, 11 Apr 2023 19:21:00 GMT  
		Size: 69.4 MB (69379392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb21b908980a44e421950e4143abc076d4fc74d81e34760821625dcda884fd`  
		Last Modified: Tue, 11 Apr 2023 19:37:39 GMT  
		Size: 7.6 MB (7603753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694cb69a4548b7d431e0b4973402c5b4d4eb4de6d721b6f57441dd06532b9004`  
		Last Modified: Thu, 11 May 2023 19:20:33 GMT  
		Size: 227.1 MB (227119166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff7d85858c755201d314c2b6170ccd483839fd858fd9b787356ee2bb161c45`  
		Last Modified: Thu, 11 May 2023 19:20:12 GMT  
		Size: 1.9 MB (1857125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350f7542abc5690705ef68d403394d6832e96610d845928b8373ce2748f1cf7`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0a14c0528b3b512a0756e4f4476042c59733970fa9bc03db495d9a4ec1cc9b`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8513b27fc3ab346613311d7b15250bc14d8129368d9b32e00a0fc11a871c72e5`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5d667d76c09ab469096d49eaa1241d21432a11258a0dc1390374cac4ee6fed`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1158f865bfd97104579313d83a4c97e4ed00f6d4e89c1b86442e4abe377f1934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303430627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34933066eaa1e505b9f266514dded96564d390163140061a427a04c0d217f632`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 11 Apr 2023 20:23:16 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 11 May 2023 19:39:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Thu, 11 May 2023 19:39:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 11 May 2023 19:39:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:39:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 May 2023 19:39:47 GMT
RUN mkdir -p /data/data /data/log
# Thu, 11 May 2023 19:39:47 GMT
VOLUME [/data]
# Thu, 11 May 2023 19:39:48 GMT
WORKDIR /data
# Thu, 11 May 2023 19:39:48 GMT
EXPOSE 4200 4300 5432
# Thu, 11 May 2023 19:39:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 11 May 2023 19:39:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 11 May 2023 19:39:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Thu, 11 May 2023 19:39:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 11 May 2023 19:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 May 2023 19:39:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467cf7edb3b9c6580c686624142f9e30588104828318064248595eb719e98539`  
		Last Modified: Tue, 11 Apr 2023 20:23:58 GMT  
		Size: 7.4 MB (7446001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5d224d23f5a2ab7dcf3ade977b5fdc56948df4e505d905820678087e51345a`  
		Last Modified: Thu, 11 May 2023 19:40:18 GMT  
		Size: 225.9 MB (225860546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b0c4b119cf3907b4854577f81f92a7a35f828c9c18dd5218ccc128ea6147c`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ab58e875a8ec851fe630ad03b4c867b80948808848aad5890771266aeafa7`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623f3bd1775a1f84b227476ee7d8ea642a70194a46a05609e31c84b961073fe`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba278803adb6715ed5e2d5ecda228bfaba0ea0560dadfc117c0e4bc4b92001`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c56c2fa5db059df9d7d38901ebbde681cc873733f990fe303abc6ad079dacbb`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2.8`

```console
$ docker pull crate@sha256:e6a6a9a0d6e61e54a3d117370782adc678a4c131aec82a6d2a25a0907cb81913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2.8` - linux; amd64

```console
$ docker pull crate@sha256:88936482b6005c1c54717aa3745961b22f8985d95362b0f47df7446edf9226f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305961319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b535b974f78397298c7c25c8df853301028dea402ec1b1ac0aacb87f126717`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:48 GMT
ADD file:9022dcd506469f7fa13db0072d1e4ed93f0ddf853bdd9ff02efc8d5a0345bb78 in / 
# Tue, 11 Apr 2023 19:19:49 GMT
CMD ["/bin/bash"]
# Tue, 11 Apr 2023 19:36:50 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 11 May 2023 19:19:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Thu, 11 May 2023 19:19:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 11 May 2023 19:19:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:19:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 May 2023 19:19:54 GMT
RUN mkdir -p /data/data /data/log
# Thu, 11 May 2023 19:19:54 GMT
VOLUME [/data]
# Thu, 11 May 2023 19:19:54 GMT
WORKDIR /data
# Thu, 11 May 2023 19:19:55 GMT
EXPOSE 4200 4300 5432
# Thu, 11 May 2023 19:19:55 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 11 May 2023 19:19:55 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 11 May 2023 19:19:55 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Thu, 11 May 2023 19:19:55 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 11 May 2023 19:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 May 2023 19:19:55 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:349bb8f337e406f9e6bd67c41b36a6481834ff3cf177d4eaa707dd54d730be7b`  
		Last Modified: Tue, 11 Apr 2023 19:21:00 GMT  
		Size: 69.4 MB (69379392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb21b908980a44e421950e4143abc076d4fc74d81e34760821625dcda884fd`  
		Last Modified: Tue, 11 Apr 2023 19:37:39 GMT  
		Size: 7.6 MB (7603753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694cb69a4548b7d431e0b4973402c5b4d4eb4de6d721b6f57441dd06532b9004`  
		Last Modified: Thu, 11 May 2023 19:20:33 GMT  
		Size: 227.1 MB (227119166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff7d85858c755201d314c2b6170ccd483839fd858fd9b787356ee2bb161c45`  
		Last Modified: Thu, 11 May 2023 19:20:12 GMT  
		Size: 1.9 MB (1857125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350f7542abc5690705ef68d403394d6832e96610d845928b8373ce2748f1cf7`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0a14c0528b3b512a0756e4f4476042c59733970fa9bc03db495d9a4ec1cc9b`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8513b27fc3ab346613311d7b15250bc14d8129368d9b32e00a0fc11a871c72e5`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5d667d76c09ab469096d49eaa1241d21432a11258a0dc1390374cac4ee6fed`  
		Last Modified: Thu, 11 May 2023 19:20:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1158f865bfd97104579313d83a4c97e4ed00f6d4e89c1b86442e4abe377f1934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303430627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34933066eaa1e505b9f266514dded96564d390163140061a427a04c0d217f632`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 11 Apr 2023 20:23:16 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 11 May 2023 19:39:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Thu, 11 May 2023 19:39:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 11 May 2023 19:39:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:39:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 May 2023 19:39:47 GMT
RUN mkdir -p /data/data /data/log
# Thu, 11 May 2023 19:39:47 GMT
VOLUME [/data]
# Thu, 11 May 2023 19:39:48 GMT
WORKDIR /data
# Thu, 11 May 2023 19:39:48 GMT
EXPOSE 4200 4300 5432
# Thu, 11 May 2023 19:39:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 11 May 2023 19:39:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 11 May 2023 19:39:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Thu, 11 May 2023 19:39:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 11 May 2023 19:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 May 2023 19:39:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467cf7edb3b9c6580c686624142f9e30588104828318064248595eb719e98539`  
		Last Modified: Tue, 11 Apr 2023 20:23:58 GMT  
		Size: 7.4 MB (7446001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5d224d23f5a2ab7dcf3ade977b5fdc56948df4e505d905820678087e51345a`  
		Last Modified: Thu, 11 May 2023 19:40:18 GMT  
		Size: 225.9 MB (225860546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b0c4b119cf3907b4854577f81f92a7a35f828c9c18dd5218ccc128ea6147c`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ab58e875a8ec851fe630ad03b4c867b80948808848aad5890771266aeafa7`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623f3bd1775a1f84b227476ee7d8ea642a70194a46a05609e31c84b961073fe`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba278803adb6715ed5e2d5ecda228bfaba0ea0560dadfc117c0e4bc4b92001`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c56c2fa5db059df9d7d38901ebbde681cc873733f990fe303abc6ad079dacbb`  
		Last Modified: Thu, 11 May 2023 19:40:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:1e804a25cd811349bddd0db6c30bb2810902edac3afdfab775afe980f4ff30f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:7d87b1c2ca0d8dfc795809bbe06d93fe2c16dca1ab6b9bf9f9d40ceadea749c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299004568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d5ddf89b7cbe8bdf6db2839479688e98bf2cdd9971655c7d821d8682b78cf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:48 GMT
ADD file:9022dcd506469f7fa13db0072d1e4ed93f0ddf853bdd9ff02efc8d5a0345bb78 in / 
# Tue, 11 Apr 2023 19:19:49 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:31:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:31:26 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:31:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:31:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:31:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:31:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:31:29 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:31:29 GMT
WORKDIR /data
# Tue, 02 May 2023 20:31:29 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:31:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:31:29 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:31:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:31:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:349bb8f337e406f9e6bd67c41b36a6481834ff3cf177d4eaa707dd54d730be7b`  
		Last Modified: Tue, 11 Apr 2023 19:21:00 GMT  
		Size: 69.4 MB (69379392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c77e438738daec477d13d3a1a666935db4f369769dc11fb9df26c4ad3d4b64`  
		Last Modified: Tue, 02 May 2023 20:32:01 GMT  
		Size: 442.1 KB (442063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d558cb1dd906c1edefba2c0b458a941b13b7a1c26dd64fcd7f0cb17838c1d5b`  
		Last Modified: Tue, 02 May 2023 20:32:16 GMT  
		Size: 227.3 MB (227324103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d75118beff48ecd7f7f5ed29abe189bf04097f436c17b5af2bd13a71f9cbb`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 1.9 MB (1857127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326752bb38a60534abae217f460530fe5eb8f2eef872170a0f7e4ca49ba24d98`  
		Last Modified: Tue, 02 May 2023 20:31:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc1bd60efc41fd02d2e6594d83ca4b2b35d639f2a77fea081963f85e217fe03`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf53e4a33f485cf48cdf0577d4e8ea18598cad408d597512ccdfa1cd0eff6c5`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb4a934e1178050de3674415b432fb3f10668193ca85ba6a52b1b4483b40640`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c424f27685ec3b3fcd15a0fb2658c4cd6b590865433d7ed36c18c24362d41004
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296630365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f7c496f88a9dc0a96a1452bf5efe3ede2311f8461cc54bbb4d6a0517b91a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:19:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:19:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:19:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:19:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:19:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:19:44 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:19:44 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:19:44 GMT
WORKDIR /data
# Tue, 02 May 2023 20:19:44 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:19:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:19:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:19:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:19:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:19:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:19:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e475c8d035fa600f0f96e27db480afc4a04bcb21f26c4d2f19b9972b4c8c538`  
		Last Modified: Tue, 02 May 2023 20:20:33 GMT  
		Size: 441.9 KB (441901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148f2b034147b42221819ebabb85a3f2b5ca8c35c661ba67683f7d47731ea69`  
		Last Modified: Tue, 02 May 2023 20:20:45 GMT  
		Size: 226.1 MB (226064372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715ea722b0a8ed9f5fef7f11ac365605766ee33705cb4e861ec83239a72b894`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 1.9 MB (1857129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab86006cafb0d26bfb3f3c5e2b0d4658c1970a48cf3c0cc39a01b0203634303`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec77bd664bf8b939bcc0340e31ff65860551a2420818438654572d632cd05f80`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fa558a9ee438fa8e36630ddf1fa00b9ab965383158fa57b1aebd14c6bea40a`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5d100da7eba08605af54a9e309c109bb658f17e67302205dbd5207dc90bff`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.1`

```console
$ docker pull crate@sha256:1e804a25cd811349bddd0db6c30bb2810902edac3afdfab775afe980f4ff30f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.1` - linux; amd64

```console
$ docker pull crate@sha256:7d87b1c2ca0d8dfc795809bbe06d93fe2c16dca1ab6b9bf9f9d40ceadea749c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299004568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d5ddf89b7cbe8bdf6db2839479688e98bf2cdd9971655c7d821d8682b78cf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:48 GMT
ADD file:9022dcd506469f7fa13db0072d1e4ed93f0ddf853bdd9ff02efc8d5a0345bb78 in / 
# Tue, 11 Apr 2023 19:19:49 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:31:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:31:26 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:31:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:31:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:31:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:31:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:31:29 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:31:29 GMT
WORKDIR /data
# Tue, 02 May 2023 20:31:29 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:31:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:31:29 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:31:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:31:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:349bb8f337e406f9e6bd67c41b36a6481834ff3cf177d4eaa707dd54d730be7b`  
		Last Modified: Tue, 11 Apr 2023 19:21:00 GMT  
		Size: 69.4 MB (69379392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c77e438738daec477d13d3a1a666935db4f369769dc11fb9df26c4ad3d4b64`  
		Last Modified: Tue, 02 May 2023 20:32:01 GMT  
		Size: 442.1 KB (442063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d558cb1dd906c1edefba2c0b458a941b13b7a1c26dd64fcd7f0cb17838c1d5b`  
		Last Modified: Tue, 02 May 2023 20:32:16 GMT  
		Size: 227.3 MB (227324103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d75118beff48ecd7f7f5ed29abe189bf04097f436c17b5af2bd13a71f9cbb`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 1.9 MB (1857127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326752bb38a60534abae217f460530fe5eb8f2eef872170a0f7e4ca49ba24d98`  
		Last Modified: Tue, 02 May 2023 20:31:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc1bd60efc41fd02d2e6594d83ca4b2b35d639f2a77fea081963f85e217fe03`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf53e4a33f485cf48cdf0577d4e8ea18598cad408d597512ccdfa1cd0eff6c5`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb4a934e1178050de3674415b432fb3f10668193ca85ba6a52b1b4483b40640`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c424f27685ec3b3fcd15a0fb2658c4cd6b590865433d7ed36c18c24362d41004
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296630365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f7c496f88a9dc0a96a1452bf5efe3ede2311f8461cc54bbb4d6a0517b91a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:19:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:19:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:19:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:19:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:19:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:19:44 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:19:44 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:19:44 GMT
WORKDIR /data
# Tue, 02 May 2023 20:19:44 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:19:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:19:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:19:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:19:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:19:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:19:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e475c8d035fa600f0f96e27db480afc4a04bcb21f26c4d2f19b9972b4c8c538`  
		Last Modified: Tue, 02 May 2023 20:20:33 GMT  
		Size: 441.9 KB (441901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148f2b034147b42221819ebabb85a3f2b5ca8c35c661ba67683f7d47731ea69`  
		Last Modified: Tue, 02 May 2023 20:20:45 GMT  
		Size: 226.1 MB (226064372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715ea722b0a8ed9f5fef7f11ac365605766ee33705cb4e861ec83239a72b894`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 1.9 MB (1857129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab86006cafb0d26bfb3f3c5e2b0d4658c1970a48cf3c0cc39a01b0203634303`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec77bd664bf8b939bcc0340e31ff65860551a2420818438654572d632cd05f80`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fa558a9ee438fa8e36630ddf1fa00b9ab965383158fa57b1aebd14c6bea40a`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5d100da7eba08605af54a9e309c109bb658f17e67302205dbd5207dc90bff`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:1e804a25cd811349bddd0db6c30bb2810902edac3afdfab775afe980f4ff30f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:7d87b1c2ca0d8dfc795809bbe06d93fe2c16dca1ab6b9bf9f9d40ceadea749c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299004568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d5ddf89b7cbe8bdf6db2839479688e98bf2cdd9971655c7d821d8682b78cf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:48 GMT
ADD file:9022dcd506469f7fa13db0072d1e4ed93f0ddf853bdd9ff02efc8d5a0345bb78 in / 
# Tue, 11 Apr 2023 19:19:49 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:31:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:31:26 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:31:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:31:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:31:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:31:29 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:31:29 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:31:29 GMT
WORKDIR /data
# Tue, 02 May 2023 20:31:29 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:31:29 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:31:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:31:29 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:31:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:31:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:349bb8f337e406f9e6bd67c41b36a6481834ff3cf177d4eaa707dd54d730be7b`  
		Last Modified: Tue, 11 Apr 2023 19:21:00 GMT  
		Size: 69.4 MB (69379392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c77e438738daec477d13d3a1a666935db4f369769dc11fb9df26c4ad3d4b64`  
		Last Modified: Tue, 02 May 2023 20:32:01 GMT  
		Size: 442.1 KB (442063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d558cb1dd906c1edefba2c0b458a941b13b7a1c26dd64fcd7f0cb17838c1d5b`  
		Last Modified: Tue, 02 May 2023 20:32:16 GMT  
		Size: 227.3 MB (227324103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d75118beff48ecd7f7f5ed29abe189bf04097f436c17b5af2bd13a71f9cbb`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 1.9 MB (1857127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326752bb38a60534abae217f460530fe5eb8f2eef872170a0f7e4ca49ba24d98`  
		Last Modified: Tue, 02 May 2023 20:31:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc1bd60efc41fd02d2e6594d83ca4b2b35d639f2a77fea081963f85e217fe03`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf53e4a33f485cf48cdf0577d4e8ea18598cad408d597512ccdfa1cd0eff6c5`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb4a934e1178050de3674415b432fb3f10668193ca85ba6a52b1b4483b40640`  
		Last Modified: Tue, 02 May 2023 20:31:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c424f27685ec3b3fcd15a0fb2658c4cd6b590865433d7ed36c18c24362d41004
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296630365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f7c496f88a9dc0a96a1452bf5efe3ede2311f8461cc54bbb4d6a0517b91a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 20:19:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 02 May 2023 20:19:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Tue, 02 May 2023 20:19:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 02 May 2023 20:19:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 20:19:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 May 2023 20:19:44 GMT
RUN mkdir -p /data/data /data/log
# Tue, 02 May 2023 20:19:44 GMT
VOLUME [/data]
# Tue, 02 May 2023 20:19:44 GMT
WORKDIR /data
# Tue, 02 May 2023 20:19:44 GMT
EXPOSE 4200 4300 5432
# Tue, 02 May 2023 20:19:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 02 May 2023 20:19:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 02 May 2023 20:19:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Tue, 02 May 2023 20:19:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 02 May 2023 20:19:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 20:19:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e475c8d035fa600f0f96e27db480afc4a04bcb21f26c4d2f19b9972b4c8c538`  
		Last Modified: Tue, 02 May 2023 20:20:33 GMT  
		Size: 441.9 KB (441901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148f2b034147b42221819ebabb85a3f2b5ca8c35c661ba67683f7d47731ea69`  
		Last Modified: Tue, 02 May 2023 20:20:45 GMT  
		Size: 226.1 MB (226064372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715ea722b0a8ed9f5fef7f11ac365605766ee33705cb4e861ec83239a72b894`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 1.9 MB (1857129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab86006cafb0d26bfb3f3c5e2b0d4658c1970a48cf3c0cc39a01b0203634303`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec77bd664bf8b939bcc0340e31ff65860551a2420818438654572d632cd05f80`  
		Last Modified: Tue, 02 May 2023 20:20:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fa558a9ee438fa8e36630ddf1fa00b9ab965383158fa57b1aebd14c6bea40a`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5d100da7eba08605af54a9e309c109bb658f17e67302205dbd5207dc90bff`  
		Last Modified: Tue, 02 May 2023 20:20:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
