## `crate:latest`

```console
$ docker pull crate@sha256:6a09aec74886927bfe4776790251bab9b4dbed5e06965e5749bfe70305cfebc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:2ed51d9b0502d5d1e2cad0dbabef728367075a2592a1dbbe3367aaf257d6631d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332880853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bafe2a168343e36ae040c5e817e602f7ccb8cbd60e8060751874aad0df3c53c`
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
# Wed, 15 Sep 2021 18:38:45 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.3.tar.gz.asc crate-4.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.3.tar.gz.asc     && tar -xf crate-4.6.3.tar.gz -C /crate --strip-components=1     && rm crate-4.6.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:38:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:38:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:38:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:38:52 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:38:52 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:38:52 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:38:53 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:38:53 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:38:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:38:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-08T14:23:11.431094 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.3
# Wed, 15 Sep 2021 18:38:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:38:54 GMT
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
	-	`sha256:a436df8d2f01d17a412359e416ba88701b22847dfa82abae15d8d60b7e8e55fc`  
		Last Modified: Wed, 15 Sep 2021 18:46:49 GMT  
		Size: 255.2 MB (255197364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06250c2396c1c83cc5cd46f757b83707f6aae7b22b0bcdf46b4a006bc4162f79`  
		Last Modified: Wed, 15 Sep 2021 18:46:25 GMT  
		Size: 1.6 MB (1582192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e9f9c04c082fa2b4bffd8c18794c2075525701c2367830d1e8fded1771bb6`  
		Last Modified: Wed, 15 Sep 2021 18:46:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7a57eae6917d4142c1a4f6fb2dc744a39b7b91b92b4b2b77de5a119e7e8399`  
		Last Modified: Wed, 15 Sep 2021 18:46:24 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33b247fe4a3ef6f41b413d13a4eb6eae00f9fcfe38f29c4b8ede4b7d7df7f44`  
		Last Modified: Wed, 15 Sep 2021 18:46:24 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486eb2cad3eef9342895d4d8843321197d2cc6887055c28d1f05b468842c3589`  
		Last Modified: Wed, 15 Sep 2021 18:46:24 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f91ba2cee5d9205e7e651ca52779ba829d3188434cb44d458ea7df3982451b40
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361947890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e421ff7482793294b1a8c8b3b16bac462123feefacd78d3842b4ac78de64c6c3`
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
# Wed, 15 Sep 2021 18:04:39 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.3.tar.gz.asc crate-4.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.3.tar.gz.asc     && tar -xf crate-4.6.3.tar.gz -C /crate --strip-components=1     && rm crate-4.6.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 15 Sep 2021 18:04:46 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 15 Sep 2021 18:04:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 18:04:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 15 Sep 2021 18:04:48 GMT
RUN mkdir -p /data/data /data/log
# Wed, 15 Sep 2021 18:04:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 18:04:48 GMT
WORKDIR /data
# Wed, 15 Sep 2021 18:04:48 GMT
EXPOSE 4200 4300 5432
# Wed, 15 Sep 2021 18:04:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 15 Sep 2021 18:04:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 15 Sep 2021 18:04:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-09-08T14:23:11.431094 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.3
# Wed, 15 Sep 2021 18:04:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 15 Sep 2021 18:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 18:04:49 GMT
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
	-	`sha256:f46cbe33f62a1e79fd234c8c4784b6c192f8c021404365108ee22833af524824`  
		Last Modified: Wed, 15 Sep 2021 18:15:24 GMT  
		Size: 252.0 MB (251986611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cec76741ce5fccb17bc53a1d90550546a0367c3c2a04d65d131625a66033c72`  
		Last Modified: Wed, 15 Sep 2021 18:14:57 GMT  
		Size: 1.6 MB (1582194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd6868fe401c49d14285333a070aa14ac1b54d8edd1a15df9e3a8d2767ccccf`  
		Last Modified: Wed, 15 Sep 2021 18:14:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae374577722a45220c7e25141536cd9b3b44579b92331e927ed41ad13a69cb7e`  
		Last Modified: Wed, 15 Sep 2021 18:14:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b02e83ed9f55a458e6aa3fae67199ba0080509a61c1453069015d2c5ce5090`  
		Last Modified: Wed, 15 Sep 2021 18:14:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646f7d988c306f6fec5a969496fb5c0596dfc281aff243c0db311f38c851583`  
		Last Modified: Wed, 15 Sep 2021 18:14:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
