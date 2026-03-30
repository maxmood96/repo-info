## `crate:latest`

```console
$ docker pull crate@sha256:799dfe9c5fec62aac6b78e4659f21a00b70ecdb8999cfd9a2b9d32f411866576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:546af29daa68316db4b201a8e2c0710c18d1736f7fa8a6f750e927033a72104e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244335032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040d2b434702ae51b78f8d441c3f178a7f45fd70088ec703ebd6b7650dc20141`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:30:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:31:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:31:04 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 30 Mar 2026 18:31:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:31:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:31:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:31:04 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:31:04 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:31:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:31:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:31:05 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:31:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Mon, 30 Mar 2026 18:31:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:31:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:31:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e43fdff4e29f652a960102e4e7e87dfb7b4cc03131f4419b43c60376fb7ba5`  
		Last Modified: Mon, 30 Mar 2026 18:31:25 GMT  
		Size: 17.8 MB (17831496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65705f2ff7b51f05b9466cb4686cd20d44cb2e88fe29d56b820547f0de81952`  
		Last Modified: Mon, 30 Mar 2026 18:31:28 GMT  
		Size: 151.3 MB (151298372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df071363bdf960e22a43abab0fd6176dff35ecfc116f4660cd7f3fd6c8e79c`  
		Last Modified: Mon, 30 Mar 2026 18:31:24 GMT  
		Size: 7.7 MB (7687426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bc7519d08d23d81e5ca03c9ba3b1e1fb0ba2df886c0370865fbbd9e177c742`  
		Last Modified: Mon, 30 Mar 2026 18:31:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f62ef7c663879474b6fd00aabbc125492b3d8c891c552556d2f4602d4ab83b`  
		Last Modified: Mon, 30 Mar 2026 18:31:25 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f013c8a4db5cdbc63e32e481d9b313c691bbc986fe83dbafdcb3b089fc1765a2`  
		Last Modified: Mon, 30 Mar 2026 18:31:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90422b5044a6b81e73db66bd5e3eb394ff06303efed818387c11c17668596b06`  
		Last Modified: Mon, 30 Mar 2026 18:31:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c98e28de738ab046e29715757d10b760603948f82361205647795b93c05bb990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcb8512dc20c31d07c9f50c72a7c4e292b5271b40964602de45204e36668c6d`

```dockerfile
```

-	Layers:
	-	`sha256:035e4f8785bb59922370552f691a6826ed7f6cdb1211f78b085b049ff509c3a7`  
		Last Modified: Mon, 30 Mar 2026 18:31:24 GMT  
		Size: 6.5 MB (6462633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338d94302914141d0f9a98aef7b34e12cbfafe7b2d4560481f42480a56f2817b`  
		Last Modified: Mon, 30 Mar 2026 18:31:24 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c744349a8c78a3ab05ab6f5c8bba5cf59e32c16bcae9838314122915b4e005a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240936972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6cb4b784c0732b85a1361018353308635a70d082f63db0a2a18173e00d58e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:30:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:30:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:30:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:30:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:30:47 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:30:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:30:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Mon, 30 Mar 2026 18:30:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:30:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:30:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f91910be8343917b71b0feb2a4b7d960559b8aa66f4a4661185a4b3eefd820`  
		Last Modified: Mon, 30 Mar 2026 18:31:21 GMT  
		Size: 17.9 MB (17888020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de3280e8bc64cbe9a618b1ada9a8790fb509aaef449449d95fa705c1d5c9c62`  
		Last Modified: Mon, 30 Mar 2026 18:31:26 GMT  
		Size: 149.3 MB (149270178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5196b113dc52e74cce26cecd563f600d4d613900d2646a5aea5b911aa5f531d`  
		Last Modified: Mon, 30 Mar 2026 18:31:19 GMT  
		Size: 7.7 MB (7680922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b0d57d31060e2092ad5449fcbf9c3f53ee5fcdda1a313d57b8f3c12f641687`  
		Last Modified: Mon, 30 Mar 2026 18:31:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f319f1ea67faa98d3ca40a37942d391d5e08a55dee01c6de3b7e343958d1949`  
		Last Modified: Mon, 30 Mar 2026 18:31:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e26982f0700679aa849ee185fdab746c0276ec7811129a0b4e1efef848eec9`  
		Last Modified: Mon, 30 Mar 2026 18:31:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb9ddbdc507c80328e4d9160538b5f331ce1283d74917e2a1d639eb4b4400d3`  
		Last Modified: Mon, 30 Mar 2026 18:31:21 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f0c8e86fe7801a222dc3ea59199852b7b40c25ad0079e81dc59b0aa2e1fb65ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22009cb66b62c31bc73c7549e8ba0d938cce8e447da5da84b978c73c29bf417`

```dockerfile
```

-	Layers:
	-	`sha256:12ed78cd6e74bb56a12567225a9fec1f4396d7639461c69ac9f13f82669136cf`  
		Last Modified: Mon, 30 Mar 2026 18:31:19 GMT  
		Size: 6.5 MB (6460552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bbfb26f4332e08ad5d8225870f2e871e4bbdd0ed977d3e17aab53d130a03e9d`  
		Last Modified: Mon, 30 Mar 2026 18:31:12 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
