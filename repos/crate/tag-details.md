<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.7`](#crate627)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:2b8fbd73042fb41554869e06ee785cfcb222f58534aced435d645783d9deefe7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:694133401470396e4a4fffb36067ca7a5350ebbe8b76c38950499063079d032b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243724258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61ca791c5b216677fe56df8a46dfab5287ddbd4b609156be7f140028d603ac3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 11 May 2026 17:11:36 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:36 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:36 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:36 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:36 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:36 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 11 May 2026 17:11:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aec96c50610621dc9e53e17af8c47771a8cb340af4ecb3b96b43753b8e422`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 18.4 MB (18369888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf3b51906dd6ceed09ab30641caecad31198658f8fbebb0c1de84dcd144469`  
		Last Modified: Mon, 11 May 2026 17:11:58 GMT  
		Size: 149.0 MB (149020529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83443fe91a3262e815ac121e0784e9426a6f46f42cc7601ead7afbed06d3a306`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 7.8 MB (7762725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb11b8e9561c013d916ac9fb8f54fda03887b06c788fd4f7528cbe3a18cf257`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caabc7f0f259d1d5dd3d93afb0f03f616cc52f5a6d6dbeebc6ab9653af464647`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28106bfffb3be8f3627331b3d61b5d768e5c679a4a8e8a15f3455b1d2ee55056`  
		Last Modified: Mon, 11 May 2026 17:11:56 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26d8009e83d61bf99bb27eb39bc032b55ca69972af4f9f6124e42b5657dbf3c`  
		Last Modified: Mon, 11 May 2026 17:11:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:bf2a54d724f17ee119fc02bbf8ae7c8795be80823d030257ed2238bdf4b09c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b65b6add2bb8b73eb1f05418ff414f17f56341ac873fbd3e556b3c16e28c6`

```dockerfile
```

-	Layers:
	-	`sha256:b60052e00f6af9c8ee4752852c4ec7842063b3314cdd00613e2226b0424b5709`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 6.7 MB (6652289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58a907a44786383ee464d126423ab52b2840637407e75d7820d410930692e6e`  
		Last Modified: Mon, 11 May 2026 17:11:54 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cb648f53cdbb3f99029da656f48a87400e0404770892c96594f819953ca02941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243047802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442e4e97d33022329f77108b27dbbfeed5e9219c3f2e608623fef43765b4f5ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 11 May 2026 17:11:41 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:42 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:42 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 11 May 2026 17:11:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def56d5535e41d6d4fe263f8fcb2db4d1064adf1803a63892373708d168ae3cc`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 18.4 MB (18420869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020423a242bfaa0937adadde04610e7e8edb3f7faae78d6cc81d266c24f670e5`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 149.7 MB (149712691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e99f6e6e4e4fb0ef6286f2700d11e7a2d710b8cf209f70669ea9fe9ec96616b`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d0dc290f7dc527580cc26a1dd68ae65d4a87fd08327d26dfa5dd5ae536f8e`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24a92bbdaafda26db5e5935e15882c170cce322418b6d4e6c661d2cc85e351`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dda4e683cd67f69540327b34cbfba52105986a6d10d29d934a4248ce02a29e`  
		Last Modified: Mon, 11 May 2026 17:12:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e658e229391a663d7bfbe89daed7aaaaa2ae00584a981fb6c0820d15e2b95`  
		Last Modified: Mon, 11 May 2026 17:12:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:1410e11692c67eedaaf5459cc06ff6b62ba00dcde9a1da25531e2177603140e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b58ee26337445c87d326f82ffe8995d2172be4887e539725d5ac763baac27e5`

```dockerfile
```

-	Layers:
	-	`sha256:a593beae6c3711850b66b66921321ecc9f0640e3f370f9f51bf778b7a4309480`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 6.7 MB (6650201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664f05981d18dff01918bc8c57958097bfaa5427c7b5671b3ac336609af31f26`  
		Last Modified: Mon, 11 May 2026 17:11:59 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:2b8fbd73042fb41554869e06ee785cfcb222f58534aced435d645783d9deefe7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:694133401470396e4a4fffb36067ca7a5350ebbe8b76c38950499063079d032b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243724258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61ca791c5b216677fe56df8a46dfab5287ddbd4b609156be7f140028d603ac3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 11 May 2026 17:11:36 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:36 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:36 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:36 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:36 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:36 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 11 May 2026 17:11:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aec96c50610621dc9e53e17af8c47771a8cb340af4ecb3b96b43753b8e422`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 18.4 MB (18369888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf3b51906dd6ceed09ab30641caecad31198658f8fbebb0c1de84dcd144469`  
		Last Modified: Mon, 11 May 2026 17:11:58 GMT  
		Size: 149.0 MB (149020529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83443fe91a3262e815ac121e0784e9426a6f46f42cc7601ead7afbed06d3a306`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 7.8 MB (7762725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb11b8e9561c013d916ac9fb8f54fda03887b06c788fd4f7528cbe3a18cf257`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caabc7f0f259d1d5dd3d93afb0f03f616cc52f5a6d6dbeebc6ab9653af464647`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28106bfffb3be8f3627331b3d61b5d768e5c679a4a8e8a15f3455b1d2ee55056`  
		Last Modified: Mon, 11 May 2026 17:11:56 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26d8009e83d61bf99bb27eb39bc032b55ca69972af4f9f6124e42b5657dbf3c`  
		Last Modified: Mon, 11 May 2026 17:11:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:bf2a54d724f17ee119fc02bbf8ae7c8795be80823d030257ed2238bdf4b09c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b65b6add2bb8b73eb1f05418ff414f17f56341ac873fbd3e556b3c16e28c6`

```dockerfile
```

-	Layers:
	-	`sha256:b60052e00f6af9c8ee4752852c4ec7842063b3314cdd00613e2226b0424b5709`  
		Last Modified: Mon, 11 May 2026 17:11:55 GMT  
		Size: 6.7 MB (6652289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58a907a44786383ee464d126423ab52b2840637407e75d7820d410930692e6e`  
		Last Modified: Mon, 11 May 2026 17:11:54 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cb648f53cdbb3f99029da656f48a87400e0404770892c96594f819953ca02941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243047802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442e4e97d33022329f77108b27dbbfeed5e9219c3f2e608623fef43765b4f5ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 11 May 2026 17:11:41 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:42 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:42 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 11 May 2026 17:11:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def56d5535e41d6d4fe263f8fcb2db4d1064adf1803a63892373708d168ae3cc`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 18.4 MB (18420869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020423a242bfaa0937adadde04610e7e8edb3f7faae78d6cc81d266c24f670e5`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 149.7 MB (149712691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e99f6e6e4e4fb0ef6286f2700d11e7a2d710b8cf209f70669ea9fe9ec96616b`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d0dc290f7dc527580cc26a1dd68ae65d4a87fd08327d26dfa5dd5ae536f8e`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24a92bbdaafda26db5e5935e15882c170cce322418b6d4e6c661d2cc85e351`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dda4e683cd67f69540327b34cbfba52105986a6d10d29d934a4248ce02a29e`  
		Last Modified: Mon, 11 May 2026 17:12:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e658e229391a663d7bfbe89daed7aaaaa2ae00584a981fb6c0820d15e2b95`  
		Last Modified: Mon, 11 May 2026 17:12:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:1410e11692c67eedaaf5459cc06ff6b62ba00dcde9a1da25531e2177603140e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b58ee26337445c87d326f82ffe8995d2172be4887e539725d5ac763baac27e5`

```dockerfile
```

-	Layers:
	-	`sha256:a593beae6c3711850b66b66921321ecc9f0640e3f370f9f51bf778b7a4309480`  
		Last Modified: Mon, 11 May 2026 17:12:00 GMT  
		Size: 6.7 MB (6650201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664f05981d18dff01918bc8c57958097bfaa5427c7b5671b3ac336609af31f26`  
		Last Modified: Mon, 11 May 2026 17:11:59 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:22e35e7dbc33373a9f9b26b03276de7b02474ff0e53ceccf45244ffcebdbcd4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:432bedc46b566849fb94489a995da89c749862247190d42dd2cbcb914f51667a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243852238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11f1546359fe6f91ca4566da44c084b4476e9ad89f59948bbec50f7b7c275f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:11:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 11 May 2026 17:11:47 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:47 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:47 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 11 May 2026 17:11:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297c31e1313c1238018838ffb0e6374104f40c0f2fc6c266bdea414aa251448`  
		Last Modified: Mon, 11 May 2026 17:12:06 GMT  
		Size: 18.4 MB (18369944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245932f8f85e6cef567c82eb324358237fb78980391075893d5da03218083311`  
		Last Modified: Mon, 11 May 2026 17:12:11 GMT  
		Size: 149.1 MB (149148239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77ad7aa0e7ed2a67a8d546b39d88ee540297ae1ed4e6e7e9ccc9807201f186`  
		Last Modified: Mon, 11 May 2026 17:12:06 GMT  
		Size: 7.8 MB (7762936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e75a4ae5b51e6343647fb521ce5df078a2719a4526d82d80eeecacf04b5d44`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0530f06c649c1e104b02fba651eb1c325f07bd6d3ba34b4e8a72aff7bdc85b20`  
		Last Modified: Mon, 11 May 2026 17:12:07 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1ac0d7321aacf3f7d352719a3e7a60df60b499c010d653ae60033da0dd452`  
		Last Modified: Mon, 11 May 2026 17:12:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ee5723d726309cca6e0a351a5232b4eb80bbfb64c85e83c824331862e52aca`  
		Last Modified: Mon, 11 May 2026 17:12:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:cdd9001fb75af0c10c2545ae6cda71ffeb34bccd003aec0241324695d3a7f3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f24dd124bbd6e5c3f22ab88854dc6a73ac6a08b5f8470a2940292485ae60a14`

```dockerfile
```

-	Layers:
	-	`sha256:914ce096b27bcd41e75767c9d23d7cf12da95fdd66bef186b842c87af8ad6b53`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 6.7 MB (6651073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f63e2e25d0f88a4f897a3c9ba693ea6de54b0e64754aa13deb9956897f05ddd`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:959b174f8c5645e7943a102d97e4862d685d12a3cc030c27eefaec1e7e388b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243173775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f87732e945fff3407768773e6c6c4acdeb2d8f9e7473db9846af6c077728a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:11:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:59 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 11 May 2026 17:12:02 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:12:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:12:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:12:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:12:02 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:12:02 GMT
WORKDIR /data
# Mon, 11 May 2026 17:12:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:12:03 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:12:03 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:12:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 11 May 2026 17:12:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:12:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:12:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f15c892cf7b41e5348b28b77222c7c4352f5c19f5c6fb63fcf72f174f3bd1e`  
		Last Modified: Mon, 11 May 2026 17:12:23 GMT  
		Size: 18.4 MB (18421011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f00afe104cc7b12c8f8378d3d4359d538f36a8ff8175a4a55cfde866ece2a`  
		Last Modified: Mon, 11 May 2026 17:12:25 GMT  
		Size: 149.8 MB (149838657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca7db09b133fa8dd7fd7cd010ac4f75982ff3caa99af0b253d7f37a68d21bdc`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 7.8 MB (7759129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d525b82b2a112a171f7719de8cdbad0f91d50882c496b6d2dcb85ccc27ac1f2`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7495f986bb3aa1c9d7442a950bc5582e58b0bb000829e8f7df2cafb291269684`  
		Last Modified: Mon, 11 May 2026 17:12:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1820b692eb7f45fa8e7390777ebd218922d3f916da42985309a5f7bef6c663`  
		Last Modified: Mon, 11 May 2026 17:12:24 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5775096bb7965a8db7e385b554b429d5415650eb060d192bd01fb73f75e6a80e`  
		Last Modified: Mon, 11 May 2026 17:12:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:52b05ab570672012b3fe5cd4ef72e5003e6aa382432fa27d4b52fc47f12a9cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da4957c52a556327e7413678c401adec338cd2d0a17203da397e860e4c6bf0f`

```dockerfile
```

-	Layers:
	-	`sha256:078905db16e84b2223cbcff873e58fa6897f32b0848cc1b6cfd0c7b13da15d38`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 6.6 MB (6648985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910c5f3358736c2684f1750c7f753b9e5c8b898061b095cbbf86c9a5ddd24555`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:22e35e7dbc33373a9f9b26b03276de7b02474ff0e53ceccf45244ffcebdbcd4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:432bedc46b566849fb94489a995da89c749862247190d42dd2cbcb914f51667a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243852238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11f1546359fe6f91ca4566da44c084b4476e9ad89f59948bbec50f7b7c275f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:11:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 11 May 2026 17:11:47 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:11:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:11:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:11:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:11:47 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:11:47 GMT
WORKDIR /data
# Mon, 11 May 2026 17:11:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:11:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:11:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:11:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 11 May 2026 17:11:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:11:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297c31e1313c1238018838ffb0e6374104f40c0f2fc6c266bdea414aa251448`  
		Last Modified: Mon, 11 May 2026 17:12:06 GMT  
		Size: 18.4 MB (18369944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245932f8f85e6cef567c82eb324358237fb78980391075893d5da03218083311`  
		Last Modified: Mon, 11 May 2026 17:12:11 GMT  
		Size: 149.1 MB (149148239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77ad7aa0e7ed2a67a8d546b39d88ee540297ae1ed4e6e7e9ccc9807201f186`  
		Last Modified: Mon, 11 May 2026 17:12:06 GMT  
		Size: 7.8 MB (7762936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e75a4ae5b51e6343647fb521ce5df078a2719a4526d82d80eeecacf04b5d44`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0530f06c649c1e104b02fba651eb1c325f07bd6d3ba34b4e8a72aff7bdc85b20`  
		Last Modified: Mon, 11 May 2026 17:12:07 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1ac0d7321aacf3f7d352719a3e7a60df60b499c010d653ae60033da0dd452`  
		Last Modified: Mon, 11 May 2026 17:12:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ee5723d726309cca6e0a351a5232b4eb80bbfb64c85e83c824331862e52aca`  
		Last Modified: Mon, 11 May 2026 17:12:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:cdd9001fb75af0c10c2545ae6cda71ffeb34bccd003aec0241324695d3a7f3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f24dd124bbd6e5c3f22ab88854dc6a73ac6a08b5f8470a2940292485ae60a14`

```dockerfile
```

-	Layers:
	-	`sha256:914ce096b27bcd41e75767c9d23d7cf12da95fdd66bef186b842c87af8ad6b53`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 6.7 MB (6651073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f63e2e25d0f88a4f897a3c9ba693ea6de54b0e64754aa13deb9956897f05ddd`  
		Last Modified: Mon, 11 May 2026 17:12:05 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:959b174f8c5645e7943a102d97e4862d685d12a3cc030c27eefaec1e7e388b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243173775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f87732e945fff3407768773e6c6c4acdeb2d8f9e7473db9846af6c077728a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:11:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:11:59 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 11 May 2026 17:12:02 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:12:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:12:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:12:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:12:02 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:12:02 GMT
WORKDIR /data
# Mon, 11 May 2026 17:12:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:12:03 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:12:03 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:12:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 11 May 2026 17:12:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:12:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:12:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f15c892cf7b41e5348b28b77222c7c4352f5c19f5c6fb63fcf72f174f3bd1e`  
		Last Modified: Mon, 11 May 2026 17:12:23 GMT  
		Size: 18.4 MB (18421011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f00afe104cc7b12c8f8378d3d4359d538f36a8ff8175a4a55cfde866ece2a`  
		Last Modified: Mon, 11 May 2026 17:12:25 GMT  
		Size: 149.8 MB (149838657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca7db09b133fa8dd7fd7cd010ac4f75982ff3caa99af0b253d7f37a68d21bdc`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 7.8 MB (7759129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d525b82b2a112a171f7719de8cdbad0f91d50882c496b6d2dcb85ccc27ac1f2`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7495f986bb3aa1c9d7442a950bc5582e58b0bb000829e8f7df2cafb291269684`  
		Last Modified: Mon, 11 May 2026 17:12:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1820b692eb7f45fa8e7390777ebd218922d3f916da42985309a5f7bef6c663`  
		Last Modified: Mon, 11 May 2026 17:12:24 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5775096bb7965a8db7e385b554b429d5415650eb060d192bd01fb73f75e6a80e`  
		Last Modified: Mon, 11 May 2026 17:12:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:52b05ab570672012b3fe5cd4ef72e5003e6aa382432fa27d4b52fc47f12a9cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da4957c52a556327e7413678c401adec338cd2d0a17203da397e860e4c6bf0f`

```dockerfile
```

-	Layers:
	-	`sha256:078905db16e84b2223cbcff873e58fa6897f32b0848cc1b6cfd0c7b13da15d38`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 6.6 MB (6648985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910c5f3358736c2684f1750c7f753b9e5c8b898061b095cbbf86c9a5ddd24555`  
		Last Modified: Mon, 11 May 2026 17:12:22 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:65acac647c1df37910c2a007a6a849ee4e11d1f35053d8e1f5c9b06dce0ae971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:6d8488aa91c56658a2680b28001794f420684ea5673a95c8a3e59220e6034722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246021228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad67a051d5de664e14e18a33705d1ca2fe716ae47be679c90bd999ed07978bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:44 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:44 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:44 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aec96c50610621dc9e53e17af8c47771a8cb340af4ecb3b96b43753b8e422`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 18.4 MB (18369888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b3502aa9c93208f7471144456b5be396a1e89ae0fde7c79c340bd6701f235`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 151.3 MB (151317682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59392fbf89c04a4bbfc3b54aa157130327826335e7da1d2d32c87893093a4348`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 7.8 MB (7762541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68c3e37e2edbf7ffc76e4230232c888d106ab33f1fdb64da66a3e926420137`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee17d7c3b9f3418296af6933035dfbf5396acd96f45c30c63740ebdc231bc4`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2803aa7f0486c8c3442dc3278f1fd71a4f4e9c1f43954cc91fbd847efb777f3`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6844086a72f26cd40ed769cecd08ad999ee7ea11afe1c6b0a95ed565653849`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:c89a926ef862fb2e48acff565258ab2b97c1575ec85e6951ee3441393fa2fd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224f1d382fa1008dd6f6f8fe9a2f6c5ccebd108a78cbcd8b5507783b6113c641`

```dockerfile
```

-	Layers:
	-	`sha256:6fc424509ca500c44bf414a4a20a6c0560dd3a334c5b67eef4c5d2d320445d87`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 6.7 MB (6656897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dcbc2cf1fe4e2279582f383c0c7ed720a0000bd41b45fe2e512ad0432a7585`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3bf6e2ae9629b26e25e7e28d3d35b6b57fb932fcb28f1dcca08e7c0b660460ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242617631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637cac9388c2679ba82a2c236160e8fadc6b03a07a1dd9eb624dbaabbb388202`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:54 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:54 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:54 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def56d5535e41d6d4fe263f8fcb2db4d1064adf1803a63892373708d168ae3cc`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 18.4 MB (18420869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026905ceb969cd319b4832e2a3e977f69dfa0c8ef8c97e86ffd19df39db076aa`  
		Last Modified: Mon, 11 May 2026 17:11:19 GMT  
		Size: 149.3 MB (149282716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e1abd2fe57418532fe4dfed42d3a5f930a06ba65689bb783b2ca7da0be906`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 7.8 MB (7759072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7da87a1a4c226b07810fd7c7fd6ac9ad6221a3a11e9028955f07cdcf4641a`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e5dfa0f5481df6a5910adf43cb84242e0fc58a8d0c38ff27935e65d6e3cf02`  
		Last Modified: Mon, 11 May 2026 17:11:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c26146817b745e5d7c3ecdd37463adb358588de9ac19efcfc5baf343112f772`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87baef8ebf5be9cbc06f15cc86db12ca4ad866eb3d5501ff98cb04db565feb2`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:f6b75ae17313a0639026fa9ddc1a0e692397acb1fc5fccd0a7907a0cd76142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d131095c0bf32203a59c4d7213b2aa079b3a843d557c204b98b977d96a034a9`

```dockerfile
```

-	Layers:
	-	`sha256:acfbcafe79f6f409ab358b8e4807bcd75681ef541266ecd73a3b87d80bca2c2c`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 6.7 MB (6654821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3657c827274d520d3faf9821cfd000853a9513abe202b516527ea1d22afabe`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.7`

```console
$ docker pull crate@sha256:65acac647c1df37910c2a007a6a849ee4e11d1f35053d8e1f5c9b06dce0ae971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.7` - linux; amd64

```console
$ docker pull crate@sha256:6d8488aa91c56658a2680b28001794f420684ea5673a95c8a3e59220e6034722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246021228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad67a051d5de664e14e18a33705d1ca2fe716ae47be679c90bd999ed07978bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:44 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:44 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:44 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aec96c50610621dc9e53e17af8c47771a8cb340af4ecb3b96b43753b8e422`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 18.4 MB (18369888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b3502aa9c93208f7471144456b5be396a1e89ae0fde7c79c340bd6701f235`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 151.3 MB (151317682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59392fbf89c04a4bbfc3b54aa157130327826335e7da1d2d32c87893093a4348`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 7.8 MB (7762541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68c3e37e2edbf7ffc76e4230232c888d106ab33f1fdb64da66a3e926420137`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee17d7c3b9f3418296af6933035dfbf5396acd96f45c30c63740ebdc231bc4`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2803aa7f0486c8c3442dc3278f1fd71a4f4e9c1f43954cc91fbd847efb777f3`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6844086a72f26cd40ed769cecd08ad999ee7ea11afe1c6b0a95ed565653849`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:c89a926ef862fb2e48acff565258ab2b97c1575ec85e6951ee3441393fa2fd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224f1d382fa1008dd6f6f8fe9a2f6c5ccebd108a78cbcd8b5507783b6113c641`

```dockerfile
```

-	Layers:
	-	`sha256:6fc424509ca500c44bf414a4a20a6c0560dd3a334c5b67eef4c5d2d320445d87`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 6.7 MB (6656897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dcbc2cf1fe4e2279582f383c0c7ed720a0000bd41b45fe2e512ad0432a7585`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3bf6e2ae9629b26e25e7e28d3d35b6b57fb932fcb28f1dcca08e7c0b660460ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242617631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637cac9388c2679ba82a2c236160e8fadc6b03a07a1dd9eb624dbaabbb388202`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:54 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:54 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:54 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def56d5535e41d6d4fe263f8fcb2db4d1064adf1803a63892373708d168ae3cc`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 18.4 MB (18420869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026905ceb969cd319b4832e2a3e977f69dfa0c8ef8c97e86ffd19df39db076aa`  
		Last Modified: Mon, 11 May 2026 17:11:19 GMT  
		Size: 149.3 MB (149282716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e1abd2fe57418532fe4dfed42d3a5f930a06ba65689bb783b2ca7da0be906`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 7.8 MB (7759072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7da87a1a4c226b07810fd7c7fd6ac9ad6221a3a11e9028955f07cdcf4641a`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e5dfa0f5481df6a5910adf43cb84242e0fc58a8d0c38ff27935e65d6e3cf02`  
		Last Modified: Mon, 11 May 2026 17:11:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c26146817b745e5d7c3ecdd37463adb358588de9ac19efcfc5baf343112f772`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87baef8ebf5be9cbc06f15cc86db12ca4ad866eb3d5501ff98cb04db565feb2`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:f6b75ae17313a0639026fa9ddc1a0e692397acb1fc5fccd0a7907a0cd76142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d131095c0bf32203a59c4d7213b2aa079b3a843d557c204b98b977d96a034a9`

```dockerfile
```

-	Layers:
	-	`sha256:acfbcafe79f6f409ab358b8e4807bcd75681ef541266ecd73a3b87d80bca2c2c`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 6.7 MB (6654821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3657c827274d520d3faf9821cfd000853a9513abe202b516527ea1d22afabe`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:65acac647c1df37910c2a007a6a849ee4e11d1f35053d8e1f5c9b06dce0ae971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:6d8488aa91c56658a2680b28001794f420684ea5673a95c8a3e59220e6034722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246021228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad67a051d5de664e14e18a33705d1ca2fe716ae47be679c90bd999ed07978bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:44 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:44 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:44 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aec96c50610621dc9e53e17af8c47771a8cb340af4ecb3b96b43753b8e422`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 18.4 MB (18369888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b3502aa9c93208f7471144456b5be396a1e89ae0fde7c79c340bd6701f235`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 151.3 MB (151317682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59392fbf89c04a4bbfc3b54aa157130327826335e7da1d2d32c87893093a4348`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 7.8 MB (7762541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68c3e37e2edbf7ffc76e4230232c888d106ab33f1fdb64da66a3e926420137`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee17d7c3b9f3418296af6933035dfbf5396acd96f45c30c63740ebdc231bc4`  
		Last Modified: Mon, 11 May 2026 17:11:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2803aa7f0486c8c3442dc3278f1fd71a4f4e9c1f43954cc91fbd847efb777f3`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6844086a72f26cd40ed769cecd08ad999ee7ea11afe1c6b0a95ed565653849`  
		Last Modified: Mon, 11 May 2026 17:11:06 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c89a926ef862fb2e48acff565258ab2b97c1575ec85e6951ee3441393fa2fd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224f1d382fa1008dd6f6f8fe9a2f6c5ccebd108a78cbcd8b5507783b6113c641`

```dockerfile
```

-	Layers:
	-	`sha256:6fc424509ca500c44bf414a4a20a6c0560dd3a334c5b67eef4c5d2d320445d87`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 6.7 MB (6656897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dcbc2cf1fe4e2279582f383c0c7ed720a0000bd41b45fe2e512ad0432a7585`  
		Last Modified: Mon, 11 May 2026 17:11:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3bf6e2ae9629b26e25e7e28d3d35b6b57fb932fcb28f1dcca08e7c0b660460ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242617631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637cac9388c2679ba82a2c236160e8fadc6b03a07a1dd9eb624dbaabbb388202`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 17:10:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 11 May 2026 17:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 11 May 2026 17:10:54 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 17:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 May 2026 17:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 11 May 2026 17:10:54 GMT
VOLUME [/data]
# Mon, 11 May 2026 17:10:54 GMT
WORKDIR /data
# Mon, 11 May 2026 17:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 11 May 2026 17:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 11 May 2026 17:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 11 May 2026 17:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 11 May 2026 17:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 17:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def56d5535e41d6d4fe263f8fcb2db4d1064adf1803a63892373708d168ae3cc`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 18.4 MB (18420869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026905ceb969cd319b4832e2a3e977f69dfa0c8ef8c97e86ffd19df39db076aa`  
		Last Modified: Mon, 11 May 2026 17:11:19 GMT  
		Size: 149.3 MB (149282716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e1abd2fe57418532fe4dfed42d3a5f930a06ba65689bb783b2ca7da0be906`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 7.8 MB (7759072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7da87a1a4c226b07810fd7c7fd6ac9ad6221a3a11e9028955f07cdcf4641a`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e5dfa0f5481df6a5910adf43cb84242e0fc58a8d0c38ff27935e65d6e3cf02`  
		Last Modified: Mon, 11 May 2026 17:11:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c26146817b745e5d7c3ecdd37463adb358588de9ac19efcfc5baf343112f772`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87baef8ebf5be9cbc06f15cc86db12ca4ad866eb3d5501ff98cb04db565feb2`  
		Last Modified: Mon, 11 May 2026 17:11:16 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f6b75ae17313a0639026fa9ddc1a0e692397acb1fc5fccd0a7907a0cd76142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d131095c0bf32203a59c4d7213b2aa079b3a843d557c204b98b977d96a034a9`

```dockerfile
```

-	Layers:
	-	`sha256:acfbcafe79f6f409ab358b8e4807bcd75681ef541266ecd73a3b87d80bca2c2c`  
		Last Modified: Mon, 11 May 2026 17:11:14 GMT  
		Size: 6.7 MB (6654821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3657c827274d520d3faf9821cfd000853a9513abe202b516527ea1d22afabe`  
		Last Modified: Mon, 11 May 2026 17:11:13 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
