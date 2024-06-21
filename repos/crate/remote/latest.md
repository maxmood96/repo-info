## `crate:latest`

```console
$ docker pull crate@sha256:40bbe28ea61c0374ebc24893a7ff40481ce6829bfb71e7557d7bea2a6efcc343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:c9e395861f0a229f26fa2826faa2832fd0d22fc2106d6482f877a5c32412df80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198189181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bb2770ca008a01438afd621ad1b9d2b8f01d55722b10d30b7f65d59ef7be03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f282573885649262fb9b4e0b6c346329ea4892e45f55f7a903728bccda1ad69`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c6ef00641b72c8b0ba8e11e671739fd4de83c992dacabc7a2215c2601d8148`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 127.6 MB (127647869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdefdb0f0bc3944bd0746bd7c5f979f71e15f119ef1644615ee1c62ee3f79a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca655399a56fd4ceed0e2e0c79fe2872f1199d2d12af6f721d50a90011166c71`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614aaae0c614008391cdb5e00fa4ce6588f5f40a931faa94c4127481a3695699`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ed697249cd2fd2c2cfe9244283ce72e7f6529ef3629317df21ff8c968cacc`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc07682a755e8fffd2a00ee15c9e84098d6505c3c641455b3e43d31980100ce`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b6044da2e80947ef83e55f3a8842a3348623ef869654c486ec33ed5d76337847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97beef97edc7cb022ecc82873a952ace090859cf2f08b79d5ebf95ef3c716cc9`

```dockerfile
```

-	Layers:
	-	`sha256:25b17f4a39298d3085a6860b1f9667c5f133f39fd1ce8485c619eaf27254f885`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4947789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67e01d8f2b2222864e81ce69baaaeac78fc6afe597b5cc8e033d281f2c4ebb0`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22895 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json
