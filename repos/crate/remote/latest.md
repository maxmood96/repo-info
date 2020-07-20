## `crate:latest`

```console
$ docker pull crate@sha256:75d61b06886720e4b1c1bc88e9c58464448c254c01d72652db05b7248e717c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f955849f13089d5767d39abe1aeda0fef5b538f1d9e44b102574f2c51e78d17b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333109344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5944110a145bb96d1580eaebca31db6f271b0ebf2d18ffe86eeba4dca84a8746`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:46:48 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 20 Jul 2020 19:21:26 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.1.tar.gz.asc crate-4.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.1.tar.gz.asc     && tar -xf crate-4.2.1.tar.gz -C /crate --strip-components=1     && rm crate-4.2.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 20 Jul 2020 19:21:29 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.25.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.25.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.25.0.asc crash_standalone_0.25.0     && rm -rf "$GNUPGHOME" crash_standalone_0.25.0.asc     && mv crash_standalone_0.25.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 20 Jul 2020 19:21:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jul 2020 19:21:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Jul 2020 19:21:30 GMT
RUN mkdir -p /data/data /data/log
# Mon, 20 Jul 2020 19:21:31 GMT
VOLUME [/data]
# Mon, 20 Jul 2020 19:21:31 GMT
WORKDIR /data
# Mon, 20 Jul 2020 19:21:31 GMT
EXPOSE 4200 4300 5432
# Mon, 20 Jul 2020 19:21:31 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 20 Jul 2020 19:21:31 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 20 Jul 2020 19:21:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-20T15:02:00.859248 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.1
# Mon, 20 Jul 2020 19:21:32 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 20 Jul 2020 19:21:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Jul 2020 19:21:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71257ebe0f3fef179a3b311dacc64581971431e33927c6c2107d2442d4dc1d7b`  
		Last Modified: Tue, 05 May 2020 21:51:55 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f4440cfaca4d014892813f78f3e32d3e315c8265fffb4580e03d9efd7f8638`  
		Last Modified: Mon, 20 Jul 2020 19:22:17 GMT  
		Size: 255.7 MB (255721854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d036289844d977b6e46aab9b134921edb3dbba0b0479cb7fb8c768208b352`  
		Last Modified: Mon, 20 Jul 2020 19:21:52 GMT  
		Size: 1.5 MB (1503276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be08b00e51992377f033508c597e742c37714e67bf61e3a9346929e554e40c68`  
		Last Modified: Mon, 20 Jul 2020 19:21:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da855670598a2f01f4c857c4513f15f1f9cc822332f9f8f4a224fac7a650b9`  
		Last Modified: Mon, 20 Jul 2020 19:21:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ae437c454ba32165a2d591723005539a7a880197e474769f176df1940d0b8`  
		Last Modified: Mon, 20 Jul 2020 19:21:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de6dfc56aac1c044cd5fb81384c96fe5cdb206a27318cdb87357c212785eb16`  
		Last Modified: Mon, 20 Jul 2020 19:21:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:30cbb36b5f99961dd49b3fa6e76f9fea72edfe8ecc0822faa62345192115d8f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357656657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad269e2f2f4170ec6e318c354525018d43bfa514906b9b2493f5d9b2c02a0c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 05 May 2020 21:41:25 GMT
ADD file:d64254c17612e9076d442240e4e567c0467ab6c4ca282ba5553f602805ad89ac in / 
# Tue, 05 May 2020 21:41:30 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:41:31 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:57:47 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 20 Jul 2020 19:42:42 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.2.1.tar.gz.asc crate-4.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.2.1.tar.gz.asc     && tar -xf crate-4.2.1.tar.gz -C /crate --strip-components=1     && rm crate-4.2.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 20 Jul 2020 19:43:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.25.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.25.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.25.0.asc crash_standalone_0.25.0     && rm -rf "$GNUPGHOME" crash_standalone_0.25.0.asc     && mv crash_standalone_0.25.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 20 Jul 2020 19:43:15 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jul 2020 19:43:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Jul 2020 19:43:47 GMT
RUN mkdir -p /data/data /data/log
# Mon, 20 Jul 2020 19:43:55 GMT
VOLUME [/data]
# Mon, 20 Jul 2020 19:44:02 GMT
WORKDIR /data
# Mon, 20 Jul 2020 19:44:09 GMT
EXPOSE 4200 4300 5432
# Mon, 20 Jul 2020 19:44:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 20 Jul 2020 19:44:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 20 Jul 2020 19:44:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-07-20T15:02:00.859248 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.2.1
# Mon, 20 Jul 2020 19:44:31 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 20 Jul 2020 19:44:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Jul 2020 19:44:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ae60b79047f8473e02511e923f461b869b62d2bf110b9fa282656e9f0128932d`  
		Last Modified: Tue, 05 May 2020 21:42:11 GMT  
		Size: 104.6 MB (104555376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cbdaa35d65e895b1f8cdcdae19714a1be917bbc2886d43605e27eea7c5016d`  
		Last Modified: Tue, 05 May 2020 22:01:46 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a057796721ac703bef3f1b43aa947d97f81d20ae39e989f8a3e920d66b4e4199`  
		Last Modified: Mon, 20 Jul 2020 19:46:01 GMT  
		Size: 251.6 MB (251593875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b383151964442f0d523e4c39db0849f3c79716e4b81517035ca59329fd292f4d`  
		Last Modified: Mon, 20 Jul 2020 19:45:18 GMT  
		Size: 1.5 MB (1503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7972131c9af824fd59408aa7d4a53b5b404c9f1806f148fb391a675089ceb`  
		Last Modified: Mon, 20 Jul 2020 19:45:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2111d0210fa1f399b38ebe208ff918eff829955b13149bde7c8266ad6963b415`  
		Last Modified: Mon, 20 Jul 2020 19:45:18 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413fa37a6ec63d2ce313071d2c09f8111f3bef5bcd4ccf7e4157aeef0fd372f`  
		Last Modified: Mon, 20 Jul 2020 19:45:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa816490df46a976446bfc5833472e7de7efe7c53355410c97c0486492c93c`  
		Last Modified: Mon, 20 Jul 2020 19:45:18 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
