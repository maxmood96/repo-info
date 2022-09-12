<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.7`](#crate47)
-	[`crate:4.7.3`](#crate473)
-	[`crate:4.8`](#crate48)
-	[`crate:4.8.3`](#crate483)
-	[`crate:5.0`](#crate50)
-	[`crate:5.0.1`](#crate501)
-	[`crate:latest`](#cratelatest)

## `crate:4.7`

```console
$ docker pull crate@sha256:2078450066279764db4bca22840fd0fbd5cc45167577205fbcfa37d571a3a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.7` - linux; amd64

```console
$ docker pull crate@sha256:43fb05ab45d1e9cd343b586b04ea608e6ba6577a989d2131e27631df2bb427d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378498279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894a71bc691be6203a9910f8294c22c5e8914e451ddaaea4a33d5eca38e26f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 02:19:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:46 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:46 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:46 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:46 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 02:19:47 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6b95f3386f2cd7959b406edc0cf7f12f9e8bef49197782fbb7b4689900524`  
		Last Modified: Wed, 01 Jun 2022 02:20:56 GMT  
		Size: 224.3 MB (224345961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dcdaf46f2cda8f038a6b5733adbaf57a7df63e555ac6bc200924a995417a3e`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 1.7 MB (1710770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d0adbec4d92e5eef0118b814d2c672aa63b0f68bb582aab2ee58877400bce9`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557505f940c3fe820fbf57a025f486a625df83940521bf3509da94e12b9f62a`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659873cff32f66bb0e2825b6f27d7cfa7b276aabdae7bd9c921fd11fc91753b`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0eb1fcd3de4227b7b4bd74a1f49d85f03e9ea1a5a7a1b2dd882364ef2be1e1`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6e5201e139fa9aebec01518fdcd2fc2c0bebf722f2de31b9bbaee31ac51a2b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677268672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231cf819dd48ee73009f86e05906351cfaeae24dbd0239087f57578234ea4ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:30:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 03:30:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:30:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:30:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:30:21 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:30:22 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:30:23 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:30:23 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:30:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:30:26 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:30:26 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 03:30:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:30:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:30:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a0546c53970e90c42dd06edca1fc95130796e58ffaef91bac0c74f560e18b0`  
		Last Modified: Wed, 01 Jun 2022 03:32:14 GMT  
		Size: 223.1 MB (223120525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6b93b24ed17c5809c900abbcb49ca625ffaaacf3282098013e96830de40359`  
		Last Modified: Wed, 01 Jun 2022 03:31:51 GMT  
		Size: 1.7 MB (1709338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2dc37ac1d8de177c73a57e7b9f755df1a30c2037ab362d94924202c6c67975`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b518f803547ff7d4156632269149131ca438cd16d70dc2059f22bc6e025537a`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef8e7842badd444824bf4ba171e7c3f29823d4487e2079f9d5cd71fc94ac0f`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc0735067d3a7caa3c2087750e9bfbbc644d19ab81c27800f6ebe2a1ec27242`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.7.3`

```console
$ docker pull crate@sha256:2078450066279764db4bca22840fd0fbd5cc45167577205fbcfa37d571a3a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.7.3` - linux; amd64

```console
$ docker pull crate@sha256:43fb05ab45d1e9cd343b586b04ea608e6ba6577a989d2131e27631df2bb427d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378498279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894a71bc691be6203a9910f8294c22c5e8914e451ddaaea4a33d5eca38e26f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 02:19:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:46 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:46 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:46 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:46 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 02:19:47 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6b95f3386f2cd7959b406edc0cf7f12f9e8bef49197782fbb7b4689900524`  
		Last Modified: Wed, 01 Jun 2022 02:20:56 GMT  
		Size: 224.3 MB (224345961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dcdaf46f2cda8f038a6b5733adbaf57a7df63e555ac6bc200924a995417a3e`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 1.7 MB (1710770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d0adbec4d92e5eef0118b814d2c672aa63b0f68bb582aab2ee58877400bce9`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557505f940c3fe820fbf57a025f486a625df83940521bf3509da94e12b9f62a`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659873cff32f66bb0e2825b6f27d7cfa7b276aabdae7bd9c921fd11fc91753b`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0eb1fcd3de4227b7b4bd74a1f49d85f03e9ea1a5a7a1b2dd882364ef2be1e1`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.7.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6e5201e139fa9aebec01518fdcd2fc2c0bebf722f2de31b9bbaee31ac51a2b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677268672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231cf819dd48ee73009f86e05906351cfaeae24dbd0239087f57578234ea4ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:30:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 03:30:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:30:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:30:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:30:21 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:30:22 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:30:23 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:30:23 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:30:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:30:26 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:30:26 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 03:30:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:30:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:30:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a0546c53970e90c42dd06edca1fc95130796e58ffaef91bac0c74f560e18b0`  
		Last Modified: Wed, 01 Jun 2022 03:32:14 GMT  
		Size: 223.1 MB (223120525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6b93b24ed17c5809c900abbcb49ca625ffaaacf3282098013e96830de40359`  
		Last Modified: Wed, 01 Jun 2022 03:31:51 GMT  
		Size: 1.7 MB (1709338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2dc37ac1d8de177c73a57e7b9f755df1a30c2037ab362d94924202c6c67975`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b518f803547ff7d4156632269149131ca438cd16d70dc2059f22bc6e025537a`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef8e7842badd444824bf4ba171e7c3f29823d4487e2079f9d5cd71fc94ac0f`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc0735067d3a7caa3c2087750e9bfbbc644d19ab81c27800f6ebe2a1ec27242`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8`

```console
$ docker pull crate@sha256:924ab1b55c408289c69096e6a1882c849c332d9c6eea94e206b32096ab97fc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8` - linux; amd64

```console
$ docker pull crate@sha256:51de135d92ba3a599edf7d3f910423d4e3e59829960dab1fc6d83adb59eb90eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366610269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d511426f93ae9c8ec08b29433b4f5f377194021b7660dbe66809c28f27502a6f`
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
# Mon, 12 Sep 2022 19:21:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.3.tar.gz.asc crate-4.8.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.3.tar.gz.asc     && tar -xf crate-4.8.3.tar.gz -C /crate --strip-components=1     && rm crate-4.8.3.tar.gz
# Mon, 12 Sep 2022 19:21:52 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 19:21:52 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 19:21:52 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 19:21:52 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 19:21:52 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 19:21:53 GMT
WORKDIR /data
# Mon, 12 Sep 2022 19:21:53 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 19:21:53 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 19:21:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 19:21:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T10:02:40.562035 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.3
# Mon, 12 Sep 2022 19:21:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 19:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:21:53 GMT
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
	-	`sha256:458ba81c152f923c5ce83308590409621afd3e60df9bbfcce6968c2d66a62955`  
		Last Modified: Mon, 12 Sep 2022 19:23:02 GMT  
		Size: 211.7 MB (211651116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2579a248b10d93060752cab2b2d576c1ae33b4589b3453b2dca78bfbe98967`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 1.7 MB (1710761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188fe8d710e13d7f7df73e48cf841f9316b6fa3dd8bd601d650e221f523c0058`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18efbc4be5b1f838e692eaf85f11a22c48c06545bd55dc1bb635a2e4da02b87c`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d464fbe1e6f306c3e75a9fdb999504c022d8f5e9ef3e2e63a4052e1263de2574`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774998dc0bfa7fcd18f9033ee460c49f07e42eded8b93e03504666558a97b3b`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:86ceb9bffb197395de9fcdd4c70de31514fa755bfb872514a13ac5c165d529fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665196266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60806e485a21993d671e83e81235c657292bc3f158a34efc36bde0e7d9ee974e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 18:41:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 12 Sep 2022 18:43:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.3.tar.gz.asc crate-4.8.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.3.tar.gz.asc     && tar -xf crate-4.8.3.tar.gz -C /crate --strip-components=1     && rm crate-4.8.3.tar.gz
# Mon, 12 Sep 2022 18:43:10 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 18:43:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 18:43:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 18:43:14 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 18:43:14 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 18:43:15 GMT
WORKDIR /data
# Mon, 12 Sep 2022 18:43:16 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 18:43:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 18:43:19 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 18:43:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T10:02:40.562035 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.3
# Mon, 12 Sep 2022 18:43:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 18:43:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:43:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd238cd1f3b3e268d51c624ab3e844a43301b4842b7ce7a77ec4a3f87d42d8`  
		Last Modified: Mon, 12 Sep 2022 18:44:32 GMT  
		Size: 344.7 MB (344689460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb81132778d87faac4a9dbc750256ae810e97ca17b103da319af8c47102691c1`  
		Last Modified: Mon, 12 Sep 2022 18:45:09 GMT  
		Size: 210.4 MB (210420672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7068082ca355502e7a059943ddbac78235db4c372f869c5cd7cd6ae19569cd2f`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e66e0e79979218bc4b22fecd78c0c1bbd8846b529e737e6a591c8ec605ee46`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f87e399b0871c7d6907f11bbf9ad699d0d9992935429dbd7258ddc3b17a4832`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fbae437f4f0dfbdbc80425d0ffc9423faaed710286b53cc99f226954f36954`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cdce8f5c4a39aceeb5ca22ed2e0234a0a72aefa07558a6931fba5b528b2db0`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8.3`

```console
$ docker pull crate@sha256:924ab1b55c408289c69096e6a1882c849c332d9c6eea94e206b32096ab97fc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8.3` - linux; amd64

```console
$ docker pull crate@sha256:51de135d92ba3a599edf7d3f910423d4e3e59829960dab1fc6d83adb59eb90eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366610269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d511426f93ae9c8ec08b29433b4f5f377194021b7660dbe66809c28f27502a6f`
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
# Mon, 12 Sep 2022 19:21:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.3.tar.gz.asc crate-4.8.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.3.tar.gz.asc     && tar -xf crate-4.8.3.tar.gz -C /crate --strip-components=1     && rm crate-4.8.3.tar.gz
# Mon, 12 Sep 2022 19:21:52 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 19:21:52 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 19:21:52 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 19:21:52 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 19:21:52 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 19:21:53 GMT
WORKDIR /data
# Mon, 12 Sep 2022 19:21:53 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 19:21:53 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 19:21:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 19:21:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T10:02:40.562035 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.3
# Mon, 12 Sep 2022 19:21:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 19:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:21:53 GMT
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
	-	`sha256:458ba81c152f923c5ce83308590409621afd3e60df9bbfcce6968c2d66a62955`  
		Last Modified: Mon, 12 Sep 2022 19:23:02 GMT  
		Size: 211.7 MB (211651116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2579a248b10d93060752cab2b2d576c1ae33b4589b3453b2dca78bfbe98967`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 1.7 MB (1710761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188fe8d710e13d7f7df73e48cf841f9316b6fa3dd8bd601d650e221f523c0058`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18efbc4be5b1f838e692eaf85f11a22c48c06545bd55dc1bb635a2e4da02b87c`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d464fbe1e6f306c3e75a9fdb999504c022d8f5e9ef3e2e63a4052e1263de2574`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774998dc0bfa7fcd18f9033ee460c49f07e42eded8b93e03504666558a97b3b`  
		Last Modified: Mon, 12 Sep 2022 19:22:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:86ceb9bffb197395de9fcdd4c70de31514fa755bfb872514a13ac5c165d529fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665196266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60806e485a21993d671e83e81235c657292bc3f158a34efc36bde0e7d9ee974e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 18:41:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 12 Sep 2022 18:43:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.3.tar.gz.asc crate-4.8.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.3.tar.gz.asc     && tar -xf crate-4.8.3.tar.gz -C /crate --strip-components=1     && rm crate-4.8.3.tar.gz
# Mon, 12 Sep 2022 18:43:10 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 18:43:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 18:43:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 18:43:14 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 18:43:14 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 18:43:15 GMT
WORKDIR /data
# Mon, 12 Sep 2022 18:43:16 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 18:43:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 18:43:19 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 18:43:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T10:02:40.562035 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.3
# Mon, 12 Sep 2022 18:43:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 18:43:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:43:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd238cd1f3b3e268d51c624ab3e844a43301b4842b7ce7a77ec4a3f87d42d8`  
		Last Modified: Mon, 12 Sep 2022 18:44:32 GMT  
		Size: 344.7 MB (344689460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb81132778d87faac4a9dbc750256ae810e97ca17b103da319af8c47102691c1`  
		Last Modified: Mon, 12 Sep 2022 18:45:09 GMT  
		Size: 210.4 MB (210420672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7068082ca355502e7a059943ddbac78235db4c372f869c5cd7cd6ae19569cd2f`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e66e0e79979218bc4b22fecd78c0c1bbd8846b529e737e6a591c8ec605ee46`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f87e399b0871c7d6907f11bbf9ad699d0d9992935429dbd7258ddc3b17a4832`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fbae437f4f0dfbdbc80425d0ffc9423faaed710286b53cc99f226954f36954`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cdce8f5c4a39aceeb5ca22ed2e0234a0a72aefa07558a6931fba5b528b2db0`  
		Last Modified: Mon, 12 Sep 2022 18:44:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.0`

```console
$ docker pull crate@sha256:07a664c82c2748b30812685b9890f73c7c2318b3e58cb241071bb3cdb781e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.0` - linux; amd64

```console
$ docker pull crate@sha256:8eff00749ee9fb04b03d2eff0f81fa42162a8fa92e5d0dc468f6536613b06d47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370947062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ecf3e00e5c0cdd8931f2aead5a18920185b292dd73bf8af776c6de3905956f`
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
# Mon, 12 Sep 2022 19:21:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 19:21:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 19:21:15 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 19:21:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 19:21:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 19:21:16 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 19:21:16 GMT
WORKDIR /data
# Mon, 12 Sep 2022 19:21:16 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 19:21:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 19:21:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 19:21:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:21:16 GMT
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
	-	`sha256:1ad7cb7e30eab2b2ac3378a7c628eb3dc4d5fc5b53e3e7f2f1febdebee31363b`  
		Last Modified: Mon, 12 Sep 2022 19:22:31 GMT  
		Size: 216.0 MB (215987903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bfc617e05ce8da351a806a436dc09969ccc8599731d083d5e96a9a5cd810a0`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 1.7 MB (1710767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110014c744df56466f096af6aa0f3c65a0a7d43a83c092bc13bd79f89f1b116c`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4bdf5799c2be1a700278371b05f9d1d632949d1a079d63250527905717410`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96949793f241882eb4508283160d812e81b41c2c2e84359ce9a29489c48db7bb`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ce21500b7805a54a4e0d1dfdaab87098c65699090c7b5c4d0825fa345e7983`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:df19f23d19e4d6138e12e853858e75506821d8486782a8ce7a9f816a49986122
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.6 MB (669623611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546206b6669b3a228ea966b4712a6eeb15b730c42800ca96087d88a87893044a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 18:41:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 12 Sep 2022 18:42:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 18:42:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 18:42:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 18:42:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 18:42:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 18:42:17 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 18:42:17 GMT
WORKDIR /data
# Mon, 12 Sep 2022 18:42:18 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 18:42:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 18:42:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 18:42:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 18:42:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 18:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd238cd1f3b3e268d51c624ab3e844a43301b4842b7ce7a77ec4a3f87d42d8`  
		Last Modified: Mon, 12 Sep 2022 18:44:32 GMT  
		Size: 344.7 MB (344689460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141c32fd483b7bbfc60e94481100c074012e2802b5a448cc92cf67b378ab4f1`  
		Last Modified: Mon, 12 Sep 2022 18:44:13 GMT  
		Size: 214.8 MB (214848017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76933e5885c8da21281ad89f901a8ec233a14671f8ad8ad01d1bfd0be8b27662`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075bbde3b4a482074eef2e8819a589efd5f60b698a845baf0a9114c681a43b52`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363d2b1f491d6b416fdb66fdd494894cea9694042f254dbb6d60efe6ecfebca1`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8879ca41640781cd42a1c1e81b28b818274e155fb67204aca30efeaca5f191`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb603f7c0161e40d75329fda34632ad4361ef7f1235cce4071c948d8f23e76`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.0.1`

```console
$ docker pull crate@sha256:07a664c82c2748b30812685b9890f73c7c2318b3e58cb241071bb3cdb781e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.0.1` - linux; amd64

```console
$ docker pull crate@sha256:8eff00749ee9fb04b03d2eff0f81fa42162a8fa92e5d0dc468f6536613b06d47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370947062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ecf3e00e5c0cdd8931f2aead5a18920185b292dd73bf8af776c6de3905956f`
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
# Mon, 12 Sep 2022 19:21:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 19:21:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 19:21:15 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 19:21:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 19:21:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 19:21:16 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 19:21:16 GMT
WORKDIR /data
# Mon, 12 Sep 2022 19:21:16 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 19:21:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 19:21:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 19:21:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:21:16 GMT
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
	-	`sha256:1ad7cb7e30eab2b2ac3378a7c628eb3dc4d5fc5b53e3e7f2f1febdebee31363b`  
		Last Modified: Mon, 12 Sep 2022 19:22:31 GMT  
		Size: 216.0 MB (215987903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bfc617e05ce8da351a806a436dc09969ccc8599731d083d5e96a9a5cd810a0`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 1.7 MB (1710767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110014c744df56466f096af6aa0f3c65a0a7d43a83c092bc13bd79f89f1b116c`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4bdf5799c2be1a700278371b05f9d1d632949d1a079d63250527905717410`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96949793f241882eb4508283160d812e81b41c2c2e84359ce9a29489c48db7bb`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ce21500b7805a54a4e0d1dfdaab87098c65699090c7b5c4d0825fa345e7983`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.0.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:df19f23d19e4d6138e12e853858e75506821d8486782a8ce7a9f816a49986122
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.6 MB (669623611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546206b6669b3a228ea966b4712a6eeb15b730c42800ca96087d88a87893044a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 18:41:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 12 Sep 2022 18:42:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 18:42:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 18:42:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 18:42:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 18:42:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 18:42:17 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 18:42:17 GMT
WORKDIR /data
# Mon, 12 Sep 2022 18:42:18 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 18:42:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 18:42:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 18:42:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 18:42:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 18:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd238cd1f3b3e268d51c624ab3e844a43301b4842b7ce7a77ec4a3f87d42d8`  
		Last Modified: Mon, 12 Sep 2022 18:44:32 GMT  
		Size: 344.7 MB (344689460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141c32fd483b7bbfc60e94481100c074012e2802b5a448cc92cf67b378ab4f1`  
		Last Modified: Mon, 12 Sep 2022 18:44:13 GMT  
		Size: 214.8 MB (214848017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76933e5885c8da21281ad89f901a8ec233a14671f8ad8ad01d1bfd0be8b27662`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075bbde3b4a482074eef2e8819a589efd5f60b698a845baf0a9114c681a43b52`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363d2b1f491d6b416fdb66fdd494894cea9694042f254dbb6d60efe6ecfebca1`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8879ca41640781cd42a1c1e81b28b818274e155fb67204aca30efeaca5f191`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb603f7c0161e40d75329fda34632ad4361ef7f1235cce4071c948d8f23e76`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:07a664c82c2748b30812685b9890f73c7c2318b3e58cb241071bb3cdb781e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:8eff00749ee9fb04b03d2eff0f81fa42162a8fa92e5d0dc468f6536613b06d47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370947062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ecf3e00e5c0cdd8931f2aead5a18920185b292dd73bf8af776c6de3905956f`
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
# Mon, 12 Sep 2022 19:21:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 19:21:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 19:21:15 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 19:21:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 19:21:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 19:21:16 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 19:21:16 GMT
WORKDIR /data
# Mon, 12 Sep 2022 19:21:16 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 19:21:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 19:21:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 19:21:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 19:21:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:21:16 GMT
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
	-	`sha256:1ad7cb7e30eab2b2ac3378a7c628eb3dc4d5fc5b53e3e7f2f1febdebee31363b`  
		Last Modified: Mon, 12 Sep 2022 19:22:31 GMT  
		Size: 216.0 MB (215987903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bfc617e05ce8da351a806a436dc09969ccc8599731d083d5e96a9a5cd810a0`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 1.7 MB (1710767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110014c744df56466f096af6aa0f3c65a0a7d43a83c092bc13bd79f89f1b116c`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4bdf5799c2be1a700278371b05f9d1d632949d1a079d63250527905717410`  
		Last Modified: Mon, 12 Sep 2022 19:22:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96949793f241882eb4508283160d812e81b41c2c2e84359ce9a29489c48db7bb`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ce21500b7805a54a4e0d1dfdaab87098c65699090c7b5c4d0825fa345e7983`  
		Last Modified: Mon, 12 Sep 2022 19:22:10 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:df19f23d19e4d6138e12e853858e75506821d8486782a8ce7a9f816a49986122
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.6 MB (669623611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546206b6669b3a228ea966b4712a6eeb15b730c42800ca96087d88a87893044a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 18:41:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 12 Sep 2022 18:42:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.1.tar.gz.asc crate-5.0.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.1.tar.gz.asc     && tar -xf crate-5.0.1.tar.gz -C /crate --strip-components=1     && rm crate-5.0.1.tar.gz
# Mon, 12 Sep 2022 18:42:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 12 Sep 2022 18:42:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Sep 2022 18:42:15 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 Sep 2022 18:42:16 GMT
RUN mkdir -p /data/data /data/log
# Mon, 12 Sep 2022 18:42:17 GMT
VOLUME [/data]
# Mon, 12 Sep 2022 18:42:17 GMT
WORKDIR /data
# Mon, 12 Sep 2022 18:42:18 GMT
EXPOSE 4200 4300 5432
# Mon, 12 Sep 2022 18:42:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 12 Sep 2022 18:42:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 12 Sep 2022 18:42:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-06T09:13:08.033412 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.1
# Mon, 12 Sep 2022 18:42:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 12 Sep 2022 18:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd238cd1f3b3e268d51c624ab3e844a43301b4842b7ce7a77ec4a3f87d42d8`  
		Last Modified: Mon, 12 Sep 2022 18:44:32 GMT  
		Size: 344.7 MB (344689460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141c32fd483b7bbfc60e94481100c074012e2802b5a448cc92cf67b378ab4f1`  
		Last Modified: Mon, 12 Sep 2022 18:44:13 GMT  
		Size: 214.8 MB (214848017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76933e5885c8da21281ad89f901a8ec233a14671f8ad8ad01d1bfd0be8b27662`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075bbde3b4a482074eef2e8819a589efd5f60b698a845baf0a9114c681a43b52`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363d2b1f491d6b416fdb66fdd494894cea9694042f254dbb6d60efe6ecfebca1`  
		Last Modified: Mon, 12 Sep 2022 18:43:51 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8879ca41640781cd42a1c1e81b28b818274e155fb67204aca30efeaca5f191`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb603f7c0161e40d75329fda34632ad4361ef7f1235cce4071c948d8f23e76`  
		Last Modified: Mon, 12 Sep 2022 18:43:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
