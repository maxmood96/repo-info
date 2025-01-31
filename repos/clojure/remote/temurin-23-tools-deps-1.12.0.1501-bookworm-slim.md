## `clojure:temurin-23-tools-deps-1.12.0.1501-bookworm-slim`

```console
$ docker pull clojure@sha256:0a422679b8e7f1b26e754a1d20dbcb70b357fb7061864266539e2ecbab830e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1501-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4ea9c52a0d13f6743017df1c6613986bd8163955377b3f239ef3d1a53f702ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58809bb20d5537b96a94c0690915150f23d164f5857d52cf605929282f5db072`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6501e3cd4f251655d59c9699c413ea629938c973560e6fae525f42d90956313`  
		Last Modified: Fri, 31 Jan 2025 02:18:23 GMT  
		Size: 165.3 MB (165316197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e596864b224d33f1fe3e90dd6046086fc3dec8abc7cb13b5fa9ee43c01c0835`  
		Last Modified: Fri, 31 Jan 2025 02:18:22 GMT  
		Size: 69.5 MB (69531509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c90822024c8a69dc1ed61a8fd5cebfc0eeffbca63bf0f1cfc5183837255c2`  
		Last Modified: Fri, 31 Jan 2025 02:18:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f59090c5c30d6d9515debef935cdcc6ceae8990a015876884f74f1e807123`  
		Last Modified: Fri, 31 Jan 2025 02:18:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:178268f98225449692ca14f2f3b32ec13c8277081242b76a094c98cc2bd86fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cd2731a36dc4d3df62d8bc24a1df025be764472a9f7bb0bec7630ff3dbe1fa`

```dockerfile
```

-	Layers:
	-	`sha256:45205969d64aef8eb311eed0a9298005130cd4aa79f697ac2523dbe8f9c16225`  
		Last Modified: Fri, 31 Jan 2025 02:18:21 GMT  
		Size: 4.9 MB (4917572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287137ff0a2c8a94c2177b688524f0dec6c1397ff832d86d1869f2499a99c7b1`  
		Last Modified: Fri, 31 Jan 2025 02:18:21 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1501-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3792cafd6f87d9a9e619ecfaff5713ff26838efad891efb2990ec33ecc7f2114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260705723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9017052c398b20386c174be8919c07b76a2ac9a8d0aa8a88114f8c597bf876`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e6607154e720c7b87f02949a8b89a82092770b07a013f7e734631efff3ec35`  
		Last Modified: Thu, 23 Jan 2025 03:54:52 GMT  
		Size: 163.3 MB (163281815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca74cb92f2a51c6a380f5f1ac44ebdb20df7eca700b01478466f206f33719ced`  
		Last Modified: Wed, 29 Jan 2025 20:58:34 GMT  
		Size: 69.4 MB (69381837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9a1e9901eddeae76e7a1f5bcb4647fea905d6cb4b786779edf07ee80fd9e05`  
		Last Modified: Wed, 29 Jan 2025 20:58:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef48ad16040fbb851170266dd53166b0263db88f320cebe6dd84975b9efd2b`  
		Last Modified: Wed, 29 Jan 2025 20:58:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:062c526404025ce210feabde1ca7dbba610ee8290c7c8be3038aaff636cb0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51239abd063f766f14c510eb93dabd760c54c31b60822538a5ba85cd8d045fb3`

```dockerfile
```

-	Layers:
	-	`sha256:7629804d973ff4ea9dd6d9398eff2cb162769b9d4b76551074a4c591ea53fb63`  
		Last Modified: Wed, 29 Jan 2025 20:58:32 GMT  
		Size: 4.9 MB (4922714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3184dcf296f3151a16a9935b6b3b5806035b565d1e9a3e713707089e35dd00`  
		Last Modified: Wed, 29 Jan 2025 20:58:32 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
