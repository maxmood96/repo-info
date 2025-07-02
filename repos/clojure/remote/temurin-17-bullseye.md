## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:8cb62c5b2a69c2f80cef0e7fab6810b3ff235bfab10adaa2112b72b6b16e0edb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8dd6a413dc907537dbd068ec8a9db1e92a659c40513530ec0998824047c21df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267800499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4616417ebadfb074aef8ae47dcd1e9437e20becbd8f52a5ed0ec8cc5187db2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed96396b24255cadce6240e231e31609b7786c8502dcb580469b7f35d24c158f`  
		Last Modified: Wed, 02 Jul 2025 13:38:44 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ebc4c36018a8defbf8e5f2f52f5310e940828e4b0f52e94008856c6d52e75d`  
		Last Modified: Wed, 02 Jul 2025 04:16:39 GMT  
		Size: 69.4 MB (69409609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02e5a593723dcfdba0dfcb30ba03c104622162174856c375bd57a19286b63df`  
		Last Modified: Wed, 02 Jul 2025 11:52:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca5d0b66bd0015dcad9f87ce1a4572a16c9849adbe9067789deabe0cad45f0`  
		Last Modified: Wed, 02 Jul 2025 11:52:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:72be7802b34cb9b8524e9e559e304cd455d9a003232444ab845eafdb0d3b34df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae0b7b177e0752f41112825e9b0c07611c05f9deeb9d3f5fe4ee067cdadd686`

```dockerfile
```

-	Layers:
	-	`sha256:731ac9f478db0dcb8e502b30ffb28cb2ea97073de76156883a1cadad3a7532b8`  
		Last Modified: Wed, 02 Jul 2025 06:37:18 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761e5579bb152e102e7e465bc06b52ce66e5f73dc2168c65ace9e842ac40fb81`  
		Last Modified: Wed, 02 Jul 2025 06:37:19 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e40f23835814f366fc62ea27821f91c65ccf3edb44a95cd215db17e9f0b60c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265303513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cdc9c8778680ba3653f6cca708b711c8db35a375c30068f91004cff8a5f5da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3380bbe3c25ada1a2dff3f510f053ddd95d5ad8e957977ce9f8800acdaf90da9`  
		Last Modified: Wed, 02 Jul 2025 12:31:15 GMT  
		Size: 143.5 MB (143512654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff7685d4937a552ca7273915d1ebb437a2bd53e043a45bc5f4d825bf146565`  
		Last Modified: Wed, 02 Jul 2025 12:37:54 GMT  
		Size: 69.5 MB (69537564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c1817d802d1a5c2b3f6baef85c9698b74c9cec7329fed76e58b15a1380cec`  
		Last Modified: Wed, 02 Jul 2025 12:37:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a61dd3065e3027af3f9cfdfa2ef13b2b837219f253a29259545c9a761f790`  
		Last Modified: Wed, 02 Jul 2025 12:37:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:89e30526544a82eeef3493807b63d848c3e293398427d32d4294afec4e9b6932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e081a885f142db017ca78a38148ef42f9414e4d6e8002498877c2bb41a3e69d1`

```dockerfile
```

-	Layers:
	-	`sha256:8ab131c46b0b7d02ae3b05d241a3b263952f384b8809df1155ae411f11c3a922`  
		Last Modified: Wed, 02 Jul 2025 15:37:27 GMT  
		Size: 7.4 MB (7400737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0dd8bcd0745ba72f9a568699507f115afc9a751672772b34420bd931a55b7f4`  
		Last Modified: Wed, 02 Jul 2025 15:37:28 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
