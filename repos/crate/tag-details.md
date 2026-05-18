<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.8`](#crate628)
-	[`crate:6.3`](#crate63)
-	[`crate:6.3.2`](#crate632)
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
$ docker pull crate@sha256:6b0032fa1ff3523cb9b738bd1c7439b1b1c6e4733e927834fa3b96f2ce0b57e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:164a724cd32197e71f925d9990d35ea49bd9f38a116f13ba3a9fea5818f390ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246036335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145be663d607b597327e3dfea82e7d5448e68f2e2f30b6e4057e2751c2a3069a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:03:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Mon, 18 May 2026 22:03:43 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:03:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:03:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:03:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:03:43 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:03:43 GMT
WORKDIR /data
# Mon, 18 May 2026 22:03:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:03:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:03:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:03:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Mon, 18 May 2026 22:03:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:03:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:03:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace433d29be7f3b515aaa81a1373bebfaa4672b520f1540c8131a36dcf6505c`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 18.4 MB (18371017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d55b6d59e4f9a368e2b1e0c8ccdf7dbcb398600f8d527cea238a69bb6e6c28`  
		Last Modified: Mon, 18 May 2026 22:04:03 GMT  
		Size: 151.3 MB (151332014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084efbabc16b30b8e8bcbe32f95bd3803c0e2a9cf41a61ea53666271bea584e0`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 7.8 MB (7762189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82201e506d544bfde8d6441cf746c2cde8be402451f2ee8ea34fd40da867321e`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5eeda985c607a8f046c034c617351d3391cd1cc43f1009b44235aeaa1f25fb7`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dccfa1bf021318f082f94812b9ff01e026a11f6bbdf4d80c26f642045181a5f`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b9e7b046c701743b11a290739cd74dfe2d56554c973a79266c95fba99f6e65`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:fb23c9b40581faab805e9188d0edcf030c176ccddfcf30819e3d856f54be4c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe8655b58df30b4d38167bd2a8df758f07801225680f5470d54f1a63c37ef78`

```dockerfile
```

-	Layers:
	-	`sha256:b1b4c56a01e8743605679490a22b32d6ad4f1426f9c2b167d6b3da8940c0b1ad`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 6.7 MB (6656601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129cd8a7611e5d2517af93200bfbb92e44d3fb0df37f02e743c9d760270d99c4`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ad64ba796956b789ebef038ed25e3d476774d4e3017fdfcabd6aef8259128bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242637768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e43e873a66c8b66af27e995a81258abfd5b1b32d250f82eefa6b1ef369b8b43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:03:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Mon, 18 May 2026 22:03:41 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:03:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:03:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:03:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:03:41 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:03:41 GMT
WORKDIR /data
# Mon, 18 May 2026 22:03:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:03:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:03:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:03:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Mon, 18 May 2026 22:03:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:03:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:03:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba130bde94cc6082a31782b594e4fab0b2dfe7aa02725913951701db1dd7d3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 18.4 MB (18422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c60d1df95fe95bd7c40b66adc90295a90279bebb617062857f74c6bda1090d`  
		Last Modified: Mon, 18 May 2026 22:04:02 GMT  
		Size: 149.3 MB (149300213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606a9c563dce9b6a9ac571645e4aa6c30cd6ee6de2173edf89d4f43d0ee87f6`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 7.8 MB (7759633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a86125967fe293a61afec653fdecb3bc9fed1ee559ebc491188210c0b9e5`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fcb8b329449fac3095e564ebf85cf7bfebdbd0081d3a550f7ae4d63d30af1`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc028171899d6cfddd8f3110c7237029e7c08abc4a5405322a8e7f3ecfb7b839`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523c52301b1e2d5573cb426b35bdc3411bbfae408d65252061cd2ac1fd893443`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:111de0290490757a093f207b90434c6ab15a41b3d69064cdb6061fea6a1e2c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987d111ea50085b50cb82641633858ae77325adce3657193ed358b6e42ec35c3`

```dockerfile
```

-	Layers:
	-	`sha256:066045f5350303be88a72f0217f244512f7d27af023c5d2a7a003129f3a563f2`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 6.7 MB (6654513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01ca47099bde2a63e7ffc873ea0ee97af61306fbf777c93cf4752467c24c7dc`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.8`

```console
$ docker pull crate@sha256:6b0032fa1ff3523cb9b738bd1c7439b1b1c6e4733e927834fa3b96f2ce0b57e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.8` - linux; amd64

```console
$ docker pull crate@sha256:164a724cd32197e71f925d9990d35ea49bd9f38a116f13ba3a9fea5818f390ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246036335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145be663d607b597327e3dfea82e7d5448e68f2e2f30b6e4057e2751c2a3069a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:03:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Mon, 18 May 2026 22:03:43 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:03:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:03:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:03:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:03:43 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:03:43 GMT
WORKDIR /data
# Mon, 18 May 2026 22:03:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:03:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:03:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:03:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Mon, 18 May 2026 22:03:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:03:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:03:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace433d29be7f3b515aaa81a1373bebfaa4672b520f1540c8131a36dcf6505c`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 18.4 MB (18371017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d55b6d59e4f9a368e2b1e0c8ccdf7dbcb398600f8d527cea238a69bb6e6c28`  
		Last Modified: Mon, 18 May 2026 22:04:03 GMT  
		Size: 151.3 MB (151332014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084efbabc16b30b8e8bcbe32f95bd3803c0e2a9cf41a61ea53666271bea584e0`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 7.8 MB (7762189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82201e506d544bfde8d6441cf746c2cde8be402451f2ee8ea34fd40da867321e`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5eeda985c607a8f046c034c617351d3391cd1cc43f1009b44235aeaa1f25fb7`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dccfa1bf021318f082f94812b9ff01e026a11f6bbdf4d80c26f642045181a5f`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b9e7b046c701743b11a290739cd74dfe2d56554c973a79266c95fba99f6e65`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:fb23c9b40581faab805e9188d0edcf030c176ccddfcf30819e3d856f54be4c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe8655b58df30b4d38167bd2a8df758f07801225680f5470d54f1a63c37ef78`

```dockerfile
```

-	Layers:
	-	`sha256:b1b4c56a01e8743605679490a22b32d6ad4f1426f9c2b167d6b3da8940c0b1ad`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 6.7 MB (6656601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129cd8a7611e5d2517af93200bfbb92e44d3fb0df37f02e743c9d760270d99c4`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ad64ba796956b789ebef038ed25e3d476774d4e3017fdfcabd6aef8259128bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242637768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e43e873a66c8b66af27e995a81258abfd5b1b32d250f82eefa6b1ef369b8b43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:03:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Mon, 18 May 2026 22:03:41 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:03:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:03:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:03:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:03:41 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:03:41 GMT
WORKDIR /data
# Mon, 18 May 2026 22:03:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:03:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:03:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:03:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Mon, 18 May 2026 22:03:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:03:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:03:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba130bde94cc6082a31782b594e4fab0b2dfe7aa02725913951701db1dd7d3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 18.4 MB (18422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c60d1df95fe95bd7c40b66adc90295a90279bebb617062857f74c6bda1090d`  
		Last Modified: Mon, 18 May 2026 22:04:02 GMT  
		Size: 149.3 MB (149300213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606a9c563dce9b6a9ac571645e4aa6c30cd6ee6de2173edf89d4f43d0ee87f6`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 7.8 MB (7759633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a86125967fe293a61afec653fdecb3bc9fed1ee559ebc491188210c0b9e5`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fcb8b329449fac3095e564ebf85cf7bfebdbd0081d3a550f7ae4d63d30af1`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc028171899d6cfddd8f3110c7237029e7c08abc4a5405322a8e7f3ecfb7b839`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523c52301b1e2d5573cb426b35bdc3411bbfae408d65252061cd2ac1fd893443`  
		Last Modified: Mon, 18 May 2026 22:04:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:111de0290490757a093f207b90434c6ab15a41b3d69064cdb6061fea6a1e2c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987d111ea50085b50cb82641633858ae77325adce3657193ed358b6e42ec35c3`

```dockerfile
```

-	Layers:
	-	`sha256:066045f5350303be88a72f0217f244512f7d27af023c5d2a7a003129f3a563f2`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 6.7 MB (6654513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01ca47099bde2a63e7ffc873ea0ee97af61306fbf777c93cf4752467c24c7dc`  
		Last Modified: Mon, 18 May 2026 22:03:59 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3`

```console
$ docker pull crate@sha256:d5cad0944515036b2fe8f68958f1eaf402b53e839e0dd1ebd4998f4c7a25c7d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3` - linux; amd64

```console
$ docker pull crate@sha256:f106135e8137fbac999230bc93c6ea50dfa610b9ab3d0f6dcd58f0ec274d9fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233773782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe876033682492b77f1511f9f3552cc56c311d1ad208d4765c68b0e8107739d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:59 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:59 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:59 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:59 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:59 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:59 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace433d29be7f3b515aaa81a1373bebfaa4672b520f1540c8131a36dcf6505c`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 18.4 MB (18371017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51d63afbe47d7d1fc3cc4674477f7d75c7aa6ec5a925ac9f3f5685bcec045b`  
		Last Modified: Mon, 18 May 2026 22:03:20 GMT  
		Size: 139.1 MB (139069159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebc42a8a11d990490234798fb30818699d1074152cf88f82c810ef8c3f32e5`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 7.8 MB (7762489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea602e48aaa0f7152028a61c7d924d3b1de0ba308c8024ab2ebda6ea4598c7`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9abdf203b5adb3fefcad7edb3accb47d783b75ea9792ddf3f3c6b07fa1e93c`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941eca13178ae40aaf25180eb81eb6a8b39bc9643b539bfebb6d1d732cb0d85`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2465d229691727e02d9737f1f6cc479dbcc996135059ae9a5ce860249d8307b`  
		Last Modified: Mon, 18 May 2026 22:03:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:0289e3176ae33d944e42507c095061873ad442c3d4f217bbd00ecffd9736aa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd89a05af1c12d43e61048bf92fe3237eb3724dc9819b34d49dcd7fd23cb752`

```dockerfile
```

-	Layers:
	-	`sha256:1cb92b6fdf123baedc35e0996eebea0fe367c19a8cba66d2aeb9177a09025d75`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cabcb23a6c33b2efa7808f354be5c19495ecb6256cba326548c094ccd1bc8cc`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4ba62c9ef24fed4d84fbf610fe4107d0c0faa48055d10b382476a2a518fccdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aed0f1815f42e8946765c2099e331a6d34bd28a2d14bf8cdc71a888c71362e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:56 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:56 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba130bde94cc6082a31782b594e4fab0b2dfe7aa02725913951701db1dd7d3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 18.4 MB (18422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7791b5d2126be065d8562ba8792402c54ded075759c6065d3b51563e216cd4ee`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 137.0 MB (137026792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b2dfc807dbbfec35af6697aa6a14368456d36469540f802f1a4b75cf3e9168`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 7.8 MB (7759088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e99d3ddae2b2417e6d185f674478dbe42249912337ba711df07d05d2139db`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70efe3b93b32813c1cc06005fe18b2bb27f4ee0a38652dca56381b8a2df9fdf3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbbd98a7d9848e93c4857d35d5f53fb8d1dd4eb682b833a370320915479363`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1153c82b3605387f7ab2f6bfc6ba36414c7b6e29c2425cf1ef412c1a98c8f950`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:831932a04e7471b3c775f91cc1831731353da9feeb2b76006cb3f424b9fe275e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591903c4ad9bbb524cc945b9afbc33ee557e17b0ea653b6eaa34b61b3ac186c5`

```dockerfile
```

-	Layers:
	-	`sha256:3af2d1bd0e8def451407d9238f672d01628e26b1cab1513f5e1c66c1f5ece7c4`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14e03492040fb476bb2bbca7e95dd897da6fff2464e9e41a35058fd0cce87520`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3.2`

```console
$ docker pull crate@sha256:d5cad0944515036b2fe8f68958f1eaf402b53e839e0dd1ebd4998f4c7a25c7d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3.2` - linux; amd64

```console
$ docker pull crate@sha256:f106135e8137fbac999230bc93c6ea50dfa610b9ab3d0f6dcd58f0ec274d9fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233773782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe876033682492b77f1511f9f3552cc56c311d1ad208d4765c68b0e8107739d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:59 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:59 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:59 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:59 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:59 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:59 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace433d29be7f3b515aaa81a1373bebfaa4672b520f1540c8131a36dcf6505c`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 18.4 MB (18371017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51d63afbe47d7d1fc3cc4674477f7d75c7aa6ec5a925ac9f3f5685bcec045b`  
		Last Modified: Mon, 18 May 2026 22:03:20 GMT  
		Size: 139.1 MB (139069159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebc42a8a11d990490234798fb30818699d1074152cf88f82c810ef8c3f32e5`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 7.8 MB (7762489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea602e48aaa0f7152028a61c7d924d3b1de0ba308c8024ab2ebda6ea4598c7`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9abdf203b5adb3fefcad7edb3accb47d783b75ea9792ddf3f3c6b07fa1e93c`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941eca13178ae40aaf25180eb81eb6a8b39bc9643b539bfebb6d1d732cb0d85`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2465d229691727e02d9737f1f6cc479dbcc996135059ae9a5ce860249d8307b`  
		Last Modified: Mon, 18 May 2026 22:03:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:0289e3176ae33d944e42507c095061873ad442c3d4f217bbd00ecffd9736aa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd89a05af1c12d43e61048bf92fe3237eb3724dc9819b34d49dcd7fd23cb752`

```dockerfile
```

-	Layers:
	-	`sha256:1cb92b6fdf123baedc35e0996eebea0fe367c19a8cba66d2aeb9177a09025d75`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cabcb23a6c33b2efa7808f354be5c19495ecb6256cba326548c094ccd1bc8cc`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4ba62c9ef24fed4d84fbf610fe4107d0c0faa48055d10b382476a2a518fccdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aed0f1815f42e8946765c2099e331a6d34bd28a2d14bf8cdc71a888c71362e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:56 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:56 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba130bde94cc6082a31782b594e4fab0b2dfe7aa02725913951701db1dd7d3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 18.4 MB (18422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7791b5d2126be065d8562ba8792402c54ded075759c6065d3b51563e216cd4ee`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 137.0 MB (137026792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b2dfc807dbbfec35af6697aa6a14368456d36469540f802f1a4b75cf3e9168`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 7.8 MB (7759088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e99d3ddae2b2417e6d185f674478dbe42249912337ba711df07d05d2139db`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70efe3b93b32813c1cc06005fe18b2bb27f4ee0a38652dca56381b8a2df9fdf3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbbd98a7d9848e93c4857d35d5f53fb8d1dd4eb682b833a370320915479363`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1153c82b3605387f7ab2f6bfc6ba36414c7b6e29c2425cf1ef412c1a98c8f950`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:831932a04e7471b3c775f91cc1831731353da9feeb2b76006cb3f424b9fe275e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591903c4ad9bbb524cc945b9afbc33ee557e17b0ea653b6eaa34b61b3ac186c5`

```dockerfile
```

-	Layers:
	-	`sha256:3af2d1bd0e8def451407d9238f672d01628e26b1cab1513f5e1c66c1f5ece7c4`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14e03492040fb476bb2bbca7e95dd897da6fff2464e9e41a35058fd0cce87520`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:d5cad0944515036b2fe8f68958f1eaf402b53e839e0dd1ebd4998f4c7a25c7d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f106135e8137fbac999230bc93c6ea50dfa610b9ab3d0f6dcd58f0ec274d9fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233773782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe876033682492b77f1511f9f3552cc56c311d1ad208d4765c68b0e8107739d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:48 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:48 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:59 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:59 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:59 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:59 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:59 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:59 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:59 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e8aad67061d40e465889e65cebd75185e8ad26b6c023cb65f91258834ef4cba1`  
		Last Modified: Mon, 11 May 2026 16:40:04 GMT  
		Size: 68.6 MB (68569238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace433d29be7f3b515aaa81a1373bebfaa4672b520f1540c8131a36dcf6505c`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 18.4 MB (18371017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51d63afbe47d7d1fc3cc4674477f7d75c7aa6ec5a925ac9f3f5685bcec045b`  
		Last Modified: Mon, 18 May 2026 22:03:20 GMT  
		Size: 139.1 MB (139069159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebc42a8a11d990490234798fb30818699d1074152cf88f82c810ef8c3f32e5`  
		Last Modified: Mon, 18 May 2026 22:03:17 GMT  
		Size: 7.8 MB (7762489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea602e48aaa0f7152028a61c7d924d3b1de0ba308c8024ab2ebda6ea4598c7`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9abdf203b5adb3fefcad7edb3accb47d783b75ea9792ddf3f3c6b07fa1e93c`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941eca13178ae40aaf25180eb81eb6a8b39bc9643b539bfebb6d1d732cb0d85`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2465d229691727e02d9737f1f6cc479dbcc996135059ae9a5ce860249d8307b`  
		Last Modified: Mon, 18 May 2026 22:03:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:0289e3176ae33d944e42507c095061873ad442c3d4f217bbd00ecffd9736aa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd89a05af1c12d43e61048bf92fe3237eb3724dc9819b34d49dcd7fd23cb752`

```dockerfile
```

-	Layers:
	-	`sha256:1cb92b6fdf123baedc35e0996eebea0fe367c19a8cba66d2aeb9177a09025d75`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cabcb23a6c33b2efa7808f354be5c19495ecb6256cba326548c094ccd1bc8cc`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4ba62c9ef24fed4d84fbf610fe4107d0c0faa48055d10b382476a2a518fccdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aed0f1815f42e8946765c2099e331a6d34bd28a2d14bf8cdc71a888c71362e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 11 May 2026 16:39:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:39:28 GMT
CMD ["/bin/bash"]
# Mon, 18 May 2026 22:02:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 18 May 2026 22:02:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Mon, 18 May 2026 22:02:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:02:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 May 2026 22:02:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 18 May 2026 22:02:56 GMT
VOLUME [/data]
# Mon, 18 May 2026 22:02:56 GMT
WORKDIR /data
# Mon, 18 May 2026 22:02:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 18 May 2026 22:02:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 18 May 2026 22:02:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Mon, 18 May 2026 22:02:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 May 2026 22:02:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 May 2026 22:02:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2507e3d88dd4d403d95441ccdbe2b598b714ce4e80881fdd787f1ad6d5c580a5`  
		Last Modified: Mon, 11 May 2026 16:39:44 GMT  
		Size: 67.2 MB (67153098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba130bde94cc6082a31782b594e4fab0b2dfe7aa02725913951701db1dd7d3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 18.4 MB (18422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7791b5d2126be065d8562ba8792402c54ded075759c6065d3b51563e216cd4ee`  
		Last Modified: Mon, 18 May 2026 22:03:18 GMT  
		Size: 137.0 MB (137026792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b2dfc807dbbfec35af6697aa6a14368456d36469540f802f1a4b75cf3e9168`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 7.8 MB (7759088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e99d3ddae2b2417e6d185f674478dbe42249912337ba711df07d05d2139db`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70efe3b93b32813c1cc06005fe18b2bb27f4ee0a38652dca56381b8a2df9fdf3`  
		Last Modified: Mon, 18 May 2026 22:03:15 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbbd98a7d9848e93c4857d35d5f53fb8d1dd4eb682b833a370320915479363`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1153c82b3605387f7ab2f6bfc6ba36414c7b6e29c2425cf1ef412c1a98c8f950`  
		Last Modified: Mon, 18 May 2026 22:03:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:831932a04e7471b3c775f91cc1831731353da9feeb2b76006cb3f424b9fe275e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591903c4ad9bbb524cc945b9afbc33ee557e17b0ea653b6eaa34b61b3ac186c5`

```dockerfile
```

-	Layers:
	-	`sha256:3af2d1bd0e8def451407d9238f672d01628e26b1cab1513f5e1c66c1f5ece7c4`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14e03492040fb476bb2bbca7e95dd897da6fff2464e9e41a35058fd0cce87520`  
		Last Modified: Mon, 18 May 2026 22:03:14 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
