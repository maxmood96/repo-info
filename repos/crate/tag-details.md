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
$ docker pull crate@sha256:8a95269ca73e785cb6af9ff19f1f82dec5c97195cf6452151e5a4562da832c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2` - linux; amd64

```console
$ docker pull crate@sha256:385bbf633200c314bce0cb9b881d5fa0e18d6d0e61faeb3139649edc1ea98b37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304832855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c6d43266a6745244461d60fb6cc90c3b7bb5fcd7dee130dfc38b7eaea74f53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:19:48 GMT
ADD file:66e52d0b794232c137dfb1e2c3f870326b5b1364c616499459d5373522577414 in / 
# Fri, 12 May 2023 23:19:48 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:36:51 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:37:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Fri, 12 May 2023 23:37:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:37:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:37:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:37:03 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:37:03 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:37:03 GMT
WORKDIR /data
# Fri, 12 May 2023 23:37:03 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:37:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:37:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:37:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Fri, 12 May 2023 23:37:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:37:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:37:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:874b82abea9e70e9bca97da85dbd63ba3fb072473ddaf2d4ef6d107848a4e853`  
		Last Modified: Fri, 12 May 2023 23:20:24 GMT  
		Size: 68.2 MB (68221234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c431cc138cf796ae51444aa0458e50c3acb8ab4442e6f20d4c7997a4f1d65686`  
		Last Modified: Fri, 12 May 2023 23:37:50 GMT  
		Size: 7.6 MB (7633496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576a90733a76a18b168ba6b533dfb905ba7084e23bb5cc19e869a02ca4e0ffe`  
		Last Modified: Fri, 12 May 2023 23:38:05 GMT  
		Size: 227.1 MB (227119125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001aad77007e43c3e47e285ef2c5aba5a6bbd03290ad73abd3cc849ce9eb356a`  
		Last Modified: Fri, 12 May 2023 23:37:47 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c12744176fecf367d9cc05291080cf1ac4efda69e3d52e28d416cc90144ba3`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d678a28851aae1441e61b5dbd1a23aad58c0a330990ffab563b48755d52ce6bd`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc406b90b823c9ee19907dc6c79b39021417f2fcebacd74af079bec4731a6275`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284fbac0ff42591a6181c844a823128eb0a4218c30b658efca4183c84965cf3`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aaef466bef80382cdbd08c8ad16e245f720129e61766fa214120c081cf049c2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302328769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22340007204ae9302e63e520d125f566667b2b1e703b0a18ba3e63fb520eb286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:39:23 GMT
ADD file:15460098fe27bb5203c30ccda7fa816f9bcb26bc0a8a403f8b0855dc24868cfc in / 
# Fri, 12 May 2023 23:39:25 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:56:10 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:56:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Fri, 12 May 2023 23:56:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:56:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:56:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:56:25 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:56:25 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:56:25 GMT
WORKDIR /data
# Fri, 12 May 2023 23:56:25 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:56:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:56:25 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:56:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Fri, 12 May 2023 23:56:25 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:56:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:56:25 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0855046dd7495052d11b9556106bc9a13cf28c73d9fa840ca92c4b19d9f279f9`  
		Last Modified: Fri, 12 May 2023 23:39:51 GMT  
		Size: 67.1 MB (67126865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f995acbc58350329f9b48ce9d2aac4570442f2946ed0212a687d7c67b8d1a7`  
		Last Modified: Fri, 12 May 2023 23:57:05 GMT  
		Size: 7.5 MB (7482357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7856d82821cbbbea4801eaddd6b74ba393fdfc38301da0e8b816b6d6bdd72752`  
		Last Modified: Fri, 12 May 2023 23:57:17 GMT  
		Size: 225.9 MB (225860546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7001332ff76b0f8b1f1733c316f9cc33a2b7f90989675a902c8859d737f381a`  
		Last Modified: Fri, 12 May 2023 23:57:03 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5ec5787859b35f954756382cca127a07e33f96a9dfaef3008bced4901d9fe3`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec435d354908ca817db7695f3b54d4b6dc16b90cfa39c889b1b9417a06d6ecb`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbc86cffaa1a16a414b7ab19fcedb2262b36b7f66e8b519045baad16911aacb`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e63da5ab02d915f6bdb9481da476d51931edcd90dadefdbedb533ef6a7cc88`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2.8`

```console
$ docker pull crate@sha256:8a95269ca73e785cb6af9ff19f1f82dec5c97195cf6452151e5a4562da832c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2.8` - linux; amd64

```console
$ docker pull crate@sha256:385bbf633200c314bce0cb9b881d5fa0e18d6d0e61faeb3139649edc1ea98b37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304832855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c6d43266a6745244461d60fb6cc90c3b7bb5fcd7dee130dfc38b7eaea74f53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:19:48 GMT
ADD file:66e52d0b794232c137dfb1e2c3f870326b5b1364c616499459d5373522577414 in / 
# Fri, 12 May 2023 23:19:48 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:36:51 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:37:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Fri, 12 May 2023 23:37:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:37:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:37:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:37:03 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:37:03 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:37:03 GMT
WORKDIR /data
# Fri, 12 May 2023 23:37:03 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:37:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:37:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:37:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Fri, 12 May 2023 23:37:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:37:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:37:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:874b82abea9e70e9bca97da85dbd63ba3fb072473ddaf2d4ef6d107848a4e853`  
		Last Modified: Fri, 12 May 2023 23:20:24 GMT  
		Size: 68.2 MB (68221234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c431cc138cf796ae51444aa0458e50c3acb8ab4442e6f20d4c7997a4f1d65686`  
		Last Modified: Fri, 12 May 2023 23:37:50 GMT  
		Size: 7.6 MB (7633496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576a90733a76a18b168ba6b533dfb905ba7084e23bb5cc19e869a02ca4e0ffe`  
		Last Modified: Fri, 12 May 2023 23:38:05 GMT  
		Size: 227.1 MB (227119125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001aad77007e43c3e47e285ef2c5aba5a6bbd03290ad73abd3cc849ce9eb356a`  
		Last Modified: Fri, 12 May 2023 23:37:47 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c12744176fecf367d9cc05291080cf1ac4efda69e3d52e28d416cc90144ba3`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d678a28851aae1441e61b5dbd1a23aad58c0a330990ffab563b48755d52ce6bd`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc406b90b823c9ee19907dc6c79b39021417f2fcebacd74af079bec4731a6275`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284fbac0ff42591a6181c844a823128eb0a4218c30b658efca4183c84965cf3`  
		Last Modified: Fri, 12 May 2023 23:37:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aaef466bef80382cdbd08c8ad16e245f720129e61766fa214120c081cf049c2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302328769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22340007204ae9302e63e520d125f566667b2b1e703b0a18ba3e63fb520eb286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:39:23 GMT
ADD file:15460098fe27bb5203c30ccda7fa816f9bcb26bc0a8a403f8b0855dc24868cfc in / 
# Fri, 12 May 2023 23:39:25 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:56:10 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:56:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.8.tar.gz.asc crate-5.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.8.tar.gz.asc     && tar -xf crate-5.2.8.tar.gz -C /crate --strip-components=1     && rm crate-5.2.8.tar.gz
# Fri, 12 May 2023 23:56:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:56:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:56:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:56:25 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:56:25 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:56:25 GMT
WORKDIR /data
# Fri, 12 May 2023 23:56:25 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:56:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:56:25 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:56:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-05-09T10:14:19.618364 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.8
# Fri, 12 May 2023 23:56:25 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:56:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:56:25 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0855046dd7495052d11b9556106bc9a13cf28c73d9fa840ca92c4b19d9f279f9`  
		Last Modified: Fri, 12 May 2023 23:39:51 GMT  
		Size: 67.1 MB (67126865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f995acbc58350329f9b48ce9d2aac4570442f2946ed0212a687d7c67b8d1a7`  
		Last Modified: Fri, 12 May 2023 23:57:05 GMT  
		Size: 7.5 MB (7482357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7856d82821cbbbea4801eaddd6b74ba393fdfc38301da0e8b816b6d6bdd72752`  
		Last Modified: Fri, 12 May 2023 23:57:17 GMT  
		Size: 225.9 MB (225860546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7001332ff76b0f8b1f1733c316f9cc33a2b7f90989675a902c8859d737f381a`  
		Last Modified: Fri, 12 May 2023 23:57:03 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5ec5787859b35f954756382cca127a07e33f96a9dfaef3008bced4901d9fe3`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec435d354908ca817db7695f3b54d4b6dc16b90cfa39c889b1b9417a06d6ecb`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbc86cffaa1a16a414b7ab19fcedb2262b36b7f66e8b519045baad16911aacb`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e63da5ab02d915f6bdb9481da476d51931edcd90dadefdbedb533ef6a7cc88`  
		Last Modified: Fri, 12 May 2023 23:57:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:97a4b915a6b8079fd301d591c6fc12fd175f37fca49e3481a2928a09c5b86efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:0a62908b34fcb232586b747b9f4d1ec687f72655238f27534150e816d293ff90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297831435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ffcb746bb2d77bceb5fc59fbd2911366da8631f165cf329c1c8f8c0f53087a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:19:48 GMT
ADD file:66e52d0b794232c137dfb1e2c3f870326b5b1364c616499459d5373522577414 in / 
# Fri, 12 May 2023 23:19:48 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:36:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:36:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:36:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:36:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:36:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:36:37 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:36:37 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:36:37 GMT
WORKDIR /data
# Fri, 12 May 2023 23:36:37 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:36:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:36:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:36:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:36:38 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:36:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:36:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:874b82abea9e70e9bca97da85dbd63ba3fb072473ddaf2d4ef6d107848a4e853`  
		Last Modified: Fri, 12 May 2023 23:20:24 GMT  
		Size: 68.2 MB (68221234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b66a041516e3ca6b7caa2a17946b9d8ea629c9bc5440291a276d192fa01bf05`  
		Last Modified: Fri, 12 May 2023 23:37:20 GMT  
		Size: 427.1 KB (427136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d656e86d4b32f70b974182497d47bd65e178c25930846f3a209d202ea4ab15`  
		Last Modified: Fri, 12 May 2023 23:37:36 GMT  
		Size: 227.3 MB (227324066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe492726a1978b56360a04ff62eddc3fe50191be07ecd7d5bdbf7abe1c5256e`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0531dd4c0538eae0eea5187ad6377245971ffe59a285483fbee056ff373b9a87`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f525b8659d0e59bb28b6249deb3d90ece5be99e4db2c2971885d2d8f11b36081`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e37de8f6ef9c6a511523214a56bd9bf0b6c1f1a8d28f4670fbb49ac2bcc5e4`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372689a5d61bbe3bc8f54a2371b0fdb83cbd7cdabadc189389b241ead6eb4a9b`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:483a8c18bd92b46bf3ff1cf5c6db0c551eedf5a5d53a00aa5ed74229a3967c6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295476177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957dfe56d95ae9e0a9946c1d3579c9e3f8d3c64d983192069c3fad86dd00eb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:39:23 GMT
ADD file:15460098fe27bb5203c30ccda7fa816f9bcb26bc0a8a403f8b0855dc24868cfc in / 
# Fri, 12 May 2023 23:39:25 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:55:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:55:55 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:55:59 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:55:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:55:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:56:00 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:56:00 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:56:00 GMT
WORKDIR /data
# Fri, 12 May 2023 23:56:00 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:56:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:56:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:56:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:56:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0855046dd7495052d11b9556106bc9a13cf28c73d9fa840ca92c4b19d9f279f9`  
		Last Modified: Fri, 12 May 2023 23:39:51 GMT  
		Size: 67.1 MB (67126865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c80989077f423662f87940d2a32edd302f1f66a1e287f5030241c4c204ee3b`  
		Last Modified: Fri, 12 May 2023 23:56:39 GMT  
		Size: 426.0 KB (425973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c4134bf5905992ce3c619c812732f4fae0e3630afc7067ebc428d1c4e50cd`  
		Last Modified: Fri, 12 May 2023 23:56:52 GMT  
		Size: 226.1 MB (226064337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf41ec40872730a18badca27de6ccf2593a4d6c15d03cb3687f6848e9616b3`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c71bdad6233116194710cdf28404ed2ed6ab3ff14b5880672b29c84c044634`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681fc0e79328ad090cd19e62e10addc07c611771f269c2e4163ee9fa7b2667d6`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3180006e1a36e5adacc35d3abbf1ebf2557926fc78ae58f83eaa9997eaf18`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367c6fb9ec87b3518a67d2644c99e139c6a42b1aaeb762581da95be1bae51ada`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.1`

```console
$ docker pull crate@sha256:97a4b915a6b8079fd301d591c6fc12fd175f37fca49e3481a2928a09c5b86efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.1` - linux; amd64

```console
$ docker pull crate@sha256:0a62908b34fcb232586b747b9f4d1ec687f72655238f27534150e816d293ff90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297831435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ffcb746bb2d77bceb5fc59fbd2911366da8631f165cf329c1c8f8c0f53087a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:19:48 GMT
ADD file:66e52d0b794232c137dfb1e2c3f870326b5b1364c616499459d5373522577414 in / 
# Fri, 12 May 2023 23:19:48 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:36:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:36:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:36:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:36:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:36:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:36:37 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:36:37 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:36:37 GMT
WORKDIR /data
# Fri, 12 May 2023 23:36:37 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:36:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:36:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:36:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:36:38 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:36:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:36:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:874b82abea9e70e9bca97da85dbd63ba3fb072473ddaf2d4ef6d107848a4e853`  
		Last Modified: Fri, 12 May 2023 23:20:24 GMT  
		Size: 68.2 MB (68221234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b66a041516e3ca6b7caa2a17946b9d8ea629c9bc5440291a276d192fa01bf05`  
		Last Modified: Fri, 12 May 2023 23:37:20 GMT  
		Size: 427.1 KB (427136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d656e86d4b32f70b974182497d47bd65e178c25930846f3a209d202ea4ab15`  
		Last Modified: Fri, 12 May 2023 23:37:36 GMT  
		Size: 227.3 MB (227324066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe492726a1978b56360a04ff62eddc3fe50191be07ecd7d5bdbf7abe1c5256e`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0531dd4c0538eae0eea5187ad6377245971ffe59a285483fbee056ff373b9a87`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f525b8659d0e59bb28b6249deb3d90ece5be99e4db2c2971885d2d8f11b36081`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e37de8f6ef9c6a511523214a56bd9bf0b6c1f1a8d28f4670fbb49ac2bcc5e4`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372689a5d61bbe3bc8f54a2371b0fdb83cbd7cdabadc189389b241ead6eb4a9b`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:483a8c18bd92b46bf3ff1cf5c6db0c551eedf5a5d53a00aa5ed74229a3967c6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295476177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957dfe56d95ae9e0a9946c1d3579c9e3f8d3c64d983192069c3fad86dd00eb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:39:23 GMT
ADD file:15460098fe27bb5203c30ccda7fa816f9bcb26bc0a8a403f8b0855dc24868cfc in / 
# Fri, 12 May 2023 23:39:25 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:55:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:55:55 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:55:59 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:55:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:55:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:56:00 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:56:00 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:56:00 GMT
WORKDIR /data
# Fri, 12 May 2023 23:56:00 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:56:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:56:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:56:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:56:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0855046dd7495052d11b9556106bc9a13cf28c73d9fa840ca92c4b19d9f279f9`  
		Last Modified: Fri, 12 May 2023 23:39:51 GMT  
		Size: 67.1 MB (67126865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c80989077f423662f87940d2a32edd302f1f66a1e287f5030241c4c204ee3b`  
		Last Modified: Fri, 12 May 2023 23:56:39 GMT  
		Size: 426.0 KB (425973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c4134bf5905992ce3c619c812732f4fae0e3630afc7067ebc428d1c4e50cd`  
		Last Modified: Fri, 12 May 2023 23:56:52 GMT  
		Size: 226.1 MB (226064337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf41ec40872730a18badca27de6ccf2593a4d6c15d03cb3687f6848e9616b3`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c71bdad6233116194710cdf28404ed2ed6ab3ff14b5880672b29c84c044634`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681fc0e79328ad090cd19e62e10addc07c611771f269c2e4163ee9fa7b2667d6`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3180006e1a36e5adacc35d3abbf1ebf2557926fc78ae58f83eaa9997eaf18`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367c6fb9ec87b3518a67d2644c99e139c6a42b1aaeb762581da95be1bae51ada`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:97a4b915a6b8079fd301d591c6fc12fd175f37fca49e3481a2928a09c5b86efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:0a62908b34fcb232586b747b9f4d1ec687f72655238f27534150e816d293ff90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297831435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ffcb746bb2d77bceb5fc59fbd2911366da8631f165cf329c1c8f8c0f53087a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:19:48 GMT
ADD file:66e52d0b794232c137dfb1e2c3f870326b5b1364c616499459d5373522577414 in / 
# Fri, 12 May 2023 23:19:48 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:36:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:36:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:36:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:36:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:36:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:36:37 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:36:37 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:36:37 GMT
WORKDIR /data
# Fri, 12 May 2023 23:36:37 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:36:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:36:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:36:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:36:38 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:36:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:36:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:874b82abea9e70e9bca97da85dbd63ba3fb072473ddaf2d4ef6d107848a4e853`  
		Last Modified: Fri, 12 May 2023 23:20:24 GMT  
		Size: 68.2 MB (68221234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b66a041516e3ca6b7caa2a17946b9d8ea629c9bc5440291a276d192fa01bf05`  
		Last Modified: Fri, 12 May 2023 23:37:20 GMT  
		Size: 427.1 KB (427136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d656e86d4b32f70b974182497d47bd65e178c25930846f3a209d202ea4ab15`  
		Last Modified: Fri, 12 May 2023 23:37:36 GMT  
		Size: 227.3 MB (227324066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe492726a1978b56360a04ff62eddc3fe50191be07ecd7d5bdbf7abe1c5256e`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 1.9 MB (1857119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0531dd4c0538eae0eea5187ad6377245971ffe59a285483fbee056ff373b9a87`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f525b8659d0e59bb28b6249deb3d90ece5be99e4db2c2971885d2d8f11b36081`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e37de8f6ef9c6a511523214a56bd9bf0b6c1f1a8d28f4670fbb49ac2bcc5e4`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372689a5d61bbe3bc8f54a2371b0fdb83cbd7cdabadc189389b241ead6eb4a9b`  
		Last Modified: Fri, 12 May 2023 23:37:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:483a8c18bd92b46bf3ff1cf5c6db0c551eedf5a5d53a00aa5ed74229a3967c6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295476177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957dfe56d95ae9e0a9946c1d3579c9e3f8d3c64d983192069c3fad86dd00eb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 May 2023 23:39:23 GMT
ADD file:15460098fe27bb5203c30ccda7fa816f9bcb26bc0a8a403f8b0855dc24868cfc in / 
# Fri, 12 May 2023 23:39:25 GMT
CMD ["/bin/bash"]
# Fri, 12 May 2023 23:55:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 May 2023 23:55:55 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.1.tar.gz.asc crate-5.3.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.1.tar.gz.asc     && tar -xf crate-5.3.1.tar.gz -C /crate --strip-components=1     && rm crate-5.3.1.tar.gz
# Fri, 12 May 2023 23:55:59 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 May 2023 23:55:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 May 2023 23:55:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 May 2023 23:56:00 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 May 2023 23:56:00 GMT
VOLUME [/data]
# Fri, 12 May 2023 23:56:00 GMT
WORKDIR /data
# Fri, 12 May 2023 23:56:00 GMT
EXPOSE 4200 4300 5432
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 May 2023 23:56:00 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 May 2023 23:56:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-28T17:43:18.942853 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.1
# Fri, 12 May 2023 23:56:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 May 2023 23:56:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 May 2023 23:56:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0855046dd7495052d11b9556106bc9a13cf28c73d9fa840ca92c4b19d9f279f9`  
		Last Modified: Fri, 12 May 2023 23:39:51 GMT  
		Size: 67.1 MB (67126865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c80989077f423662f87940d2a32edd302f1f66a1e287f5030241c4c204ee3b`  
		Last Modified: Fri, 12 May 2023 23:56:39 GMT  
		Size: 426.0 KB (425973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c4134bf5905992ce3c619c812732f4fae0e3630afc7067ebc428d1c4e50cd`  
		Last Modified: Fri, 12 May 2023 23:56:52 GMT  
		Size: 226.1 MB (226064337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf41ec40872730a18badca27de6ccf2593a4d6c15d03cb3687f6848e9616b3`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c71bdad6233116194710cdf28404ed2ed6ab3ff14b5880672b29c84c044634`  
		Last Modified: Fri, 12 May 2023 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681fc0e79328ad090cd19e62e10addc07c611771f269c2e4163ee9fa7b2667d6`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3180006e1a36e5adacc35d3abbf1ebf2557926fc78ae58f83eaa9997eaf18`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367c6fb9ec87b3518a67d2644c99e139c6a42b1aaeb762581da95be1bae51ada`  
		Last Modified: Fri, 12 May 2023 23:56:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
