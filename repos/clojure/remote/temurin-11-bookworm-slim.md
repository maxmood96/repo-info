## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:8be26c973d66efaa65756da6229b7969de00c3d3230d520134411969c434a473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79f9e927b0886d42e7d5e18e692f08370ab420da8470bdee87a3e20ea52aab9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243744979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb24ffa28a6c857110a37a373e3a7182746b6ff64808642e404030954d9b78a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:59 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cec7e97595b5a1d076db96d9172d18f6f1a28693ffafcce1c5124d297ce694`  
		Last Modified: Wed, 04 Mar 2026 17:49:35 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f3c7549d9f6c93c03b6f33fbfe6a0e38e190dfe5d587b2fe3c978d603d3593`  
		Last Modified: Wed, 04 Mar 2026 17:49:34 GMT  
		Size: 69.7 MB (69701301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0cc15565f66c6043bc51d02810ae5a4e358301ad69d65589587eaec3a4e8ef`  
		Last Modified: Wed, 04 Mar 2026 17:49:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd13002e718f52dd789bf6ad0a477d43372c52da210036840475ff7ee1460a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0016c886fc93dc46093f9ef32ae7b4da091e4e6678bd5c8e5ffa6a46c8a65fb1`

```dockerfile
```

-	Layers:
	-	`sha256:43f9c047a8e94e6b998577a57ce43f9f9e9b96071d763f83672280f309d711a1`  
		Last Modified: Wed, 04 Mar 2026 17:49:30 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610b906bc01353d7269eec82e214031557215b8fa71a9d1242fb00f3ab2f68df`  
		Last Modified: Wed, 04 Mar 2026 17:49:29 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:522bf586f2b805ca686707a57593c5884d371127ccc815393c1fcda7460cead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240306720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da80b8b2e10febd3c15054f3f89312c544a92e50a48e50a69af52b72237a1d11`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:57 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:57 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15808364fec276ea2221e9aff6b766c1faf537f97992c562c67036637fa1d0ae`  
		Last Modified: Wed, 04 Mar 2026 17:49:35 GMT  
		Size: 142.5 MB (142501433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c667f2611576176e9979617ca6bb7f845cfcae7bace21d14f267325547f55112`  
		Last Modified: Wed, 04 Mar 2026 17:49:33 GMT  
		Size: 69.7 MB (69688564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32c8e39934b1ea388fc9bf98a573c4538910af3e8e1e835d760ab29635ef95b`  
		Last Modified: Wed, 04 Mar 2026 17:49:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74bc681a7ab53a8917810c6a759213439baa3b9777da0f4b01c2366f8f22350b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57b1cec4e1171871b3cf5efd54b03278b06501df1479389df900e7c93edb599`

```dockerfile
```

-	Layers:
	-	`sha256:2ddb92b38f9f04fdbf61b0c8f285443502916b9a49ff0cb8e82eaad7d878c671`  
		Last Modified: Wed, 04 Mar 2026 17:49:31 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77faa845d39bcbc54cd057a0fa9a5011fe1da76a7cf437f88da86f8399b3071d`  
		Last Modified: Wed, 04 Mar 2026 17:49:30 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0a8de088e7ba7dac46fde7980150b5bef1490db03417dd2215e4684d773116e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240610020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f47fbf90e9cf805fb318ccb0e20b81756c3dda2edf62a429a2301b48cd4c6e5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:53:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:53:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:53:18 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:53:19 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:54:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:54:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:54:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3784054b03531384dcdf16c1e157265b18f984cdc65e456ea8837b504451c04`  
		Last Modified: Wed, 04 Mar 2026 17:54:43 GMT  
		Size: 133.0 MB (132997823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e951aff770c7fe245f32809b76dd3f2beea4c149c3d8568f33254eace9fbda25`  
		Last Modified: Wed, 04 Mar 2026 17:54:42 GMT  
		Size: 75.5 MB (75533219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1ec99449a81d16a0fcfe06ce229f63c1caf5f144ff41a8aab744deb4add9cb`  
		Last Modified: Wed, 04 Mar 2026 17:54:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b06a60e270e585cc71165e173fd8753b65aaeb4547fcd4a49672142c6d946dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0d630cb904e193404d4be9f2cb8e4e22ad578799ef017355f37be4aa7222f4`

```dockerfile
```

-	Layers:
	-	`sha256:1aae383b54346f6a765a94f1a5d37d935f4e03bb1b2894df1a336c85627ebd39`  
		Last Modified: Wed, 04 Mar 2026 17:54:39 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692563370759e6d1fc148d5b11c172481db45b8d9b437b6dd0d91075f02a1e50`  
		Last Modified: Wed, 04 Mar 2026 17:54:39 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a96d28fef6825e3214fbf3f25f4136ab8663f61935e1018dd3766a3bbd6163a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221967633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b99b4c2ecfc1e588eece79413f901b91baacce674e7830786a42fcb107bdea1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:46:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:46:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:46:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:46:59 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:46:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:47:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:47:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:47:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f84e60ce1b9ebadea7f02a516fcb5bf4d066fb6500750b175ff6967582657`  
		Last Modified: Wed, 04 Mar 2026 17:47:45 GMT  
		Size: 126.6 MB (126562047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016aba651ea82bb4faf9fe93e4cad3e5687ab6525e39a3a72dd0bbf615e6f8a3`  
		Last Modified: Wed, 04 Mar 2026 17:47:44 GMT  
		Size: 68.5 MB (68513419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9397a2f6713c4df600b4caa4edbef0de6d308688827beca5ff22604ba0f96d82`  
		Last Modified: Wed, 04 Mar 2026 17:47:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e31c314e596bde75d003d495889e9b69c89c1a48e881700b0910c79f20776cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d15003a26d7f7c88d89e40b0420da0efd5806b56c444a3546e07d42be14f0e`

```dockerfile
```

-	Layers:
	-	`sha256:f8d62525e680c0c1ac7dea4ba628b30438e9597653a5825bca1fef66699a68e2`  
		Last Modified: Wed, 04 Mar 2026 17:47:42 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cfbd075390bf5f409970d582a3288e21e731a9f4b3a148d369cb579b38f24d`  
		Last Modified: Wed, 04 Mar 2026 17:47:42 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
