## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:f1b35f86553df56edf6712afa7cdc2ccb8ff7f3e867541076cc00d9d8b3bd1cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddf97e87af5b39495d88a59f265eeb88623e35a1cb3d2eb2db2b82647d9c445d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255487883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3deec11116b45dd502f2a2031aad728d5b3cf786df8baaeb4364591cb7d81c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291cea46b602afd129310d494c55f346f02494c3e8b19474b50219fec417c4d`  
		Last Modified: Tue, 12 Nov 2024 02:50:43 GMT  
		Size: 165.3 MB (165295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d99a5cd49a1cc5171f42c83d063dbbf18939dcfd4d923ef22a24fc6267a8781`  
		Last Modified: Tue, 12 Nov 2024 02:50:41 GMT  
		Size: 58.7 MB (58740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0937d480891cced648bebb2aa849cfcde61145259dfea02dc7ebf39d7097fd`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b59efa13a915d74fe2a867205a1127d53f6aa285f4ca45dfe85dea6fa1ebace`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f3c1e0f09f4b56abbda371fffcb117993c3e87133af350d25069ff65c10496f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579174c8b259059bd29c0848881005fa56cb15d4a5be525f9324ee9e06381411`

```dockerfile
```

-	Layers:
	-	`sha256:b8d78d16e185c7dca68fd17934d5c1d0faf1804f0f8bbc3d2788e5c58f624d9e`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 5.1 MB (5130365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843b57954dd1b59292b1f4ffc25f11898e10f13e17362d2d5e376545769e6c5`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de62d32feb0bb6725113bffb771cc4bdb99546605f20275420e124c00df320a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252251964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2dfc603bcc1129d15e38e2fe61ca2944bdfe7c9a2ea2630c6ee5354abaf27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162c0c2e53d9116b8a6e9a75f05386e05340a23204bbbdf255b382a7b4cf202a`  
		Last Modified: Wed, 13 Nov 2024 01:37:11 GMT  
		Size: 163.3 MB (163281822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e69fd4627997666d8cb49d6d5b94f2cad16e73f061bffca181e807efe9adf`  
		Last Modified: Wed, 13 Nov 2024 01:40:48 GMT  
		Size: 58.9 MB (58877499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15f441aafd47ee21e65ffa38b5ebf74987082e3d5f3269b33ad4b110da1a429`  
		Last Modified: Wed, 13 Nov 2024 01:40:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0431cdda32c677114602e62c7a265bb9539affa4e86c7bf2905cdf71f01bce`  
		Last Modified: Wed, 13 Nov 2024 01:40:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd9c8e7cb0f254016d6e5d4963391d88edcf5da62648b9a7d5e9b562515c64d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44fe299be74555f96026143c2f524eea8a596731c999c7c69160a594ddeeb89`

```dockerfile
```

-	Layers:
	-	`sha256:29006ef494bf2390693560c83c5943bf577504d241d7f3318e795723489bacb1`  
		Last Modified: Wed, 13 Nov 2024 01:40:46 GMT  
		Size: 5.1 MB (5135480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceccb89ac65f1485a5d189425004356c186a66444c07ede39a234339a79098b`  
		Last Modified: Wed, 13 Nov 2024 01:40:45 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
