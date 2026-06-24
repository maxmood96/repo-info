## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:8a82fc948348d9f4d00b27d6968f03a28f78450cfaee58c46a4fbc1096bc2f55
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
$ docker pull clojure@sha256:95ad646b947abcdf96e1882cc587ca1c5f087284197325a39824084138507c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240767396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285da049dd2216cc49f33fb592bc4d701e4011e368126307a8a7a5dbc36a28d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:16:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:16:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:16:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:16:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:16:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afefdd3f2ce9de34e907ca4815572ed3ed125d9ba146b0a738f817208d310b9`  
		Last Modified: Wed, 24 Jun 2026 02:17:27 GMT  
		Size: 145.9 MB (145886223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf81c7e854f058261dbc53dad4d9a16d9129cbc8244135ac0779d25c31757b0`  
		Last Modified: Wed, 24 Jun 2026 02:17:25 GMT  
		Size: 66.6 MB (66642890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00088d995f7a699b2b4ae273fc339d3a0c2025f3b22de898ef8378cd85d82b3d`  
		Last Modified: Wed, 24 Jun 2026 02:17:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8769b84898824095d3f74ed5546f09cd82c9c14c4e531dfaa564864265704295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803024a73728f4a1bd6daac2e22518130009f03f2798b3c92de0efef63ff6380`

```dockerfile
```

-	Layers:
	-	`sha256:b614f761b1bc1f4716e186273f377e611e0eb310c7858cf4ad6299e18d46dbdf`  
		Last Modified: Wed, 24 Jun 2026 02:17:22 GMT  
		Size: 5.1 MB (5133515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62f69c1448443be99b76bea5c09fd9d100d4cd9dbf07188a834bfe3c98193c2`  
		Last Modified: Wed, 24 Jun 2026 02:17:22 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:527810b87b3ac60b3ed147e35911a5f826e689fc7eb8afa50e9bee153e0fe0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237348556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63be39e5b8eb1a43402e80d4b279c0c0fb3c0ea79e19c789ab7746ddc15726e8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:23:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:13 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae12af3d923fce2e88756054a36886b70b1ab1f5ad23ea7a906b70862440a44d`  
		Last Modified: Wed, 24 Jun 2026 02:23:50 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d5160c71ad7528de8e2ec3cae0977b14a361ca5e13fdd38c745a136fcad837`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 66.6 MB (66643335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69ba117cad3ed5d0b7f7ce0fa6290c57fe0f4f058bf806c6f429ac01b54aa86`  
		Last Modified: Wed, 24 Jun 2026 02:23:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cade00fddfc50838f48d01ddbb2238d2c92b37d042ccd05dca15fe72dcf2f570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01875981c69b7845e09b7e37578ba4c9a939c9c13e6e4f83a7423efd3f6cbf0d`

```dockerfile
```

-	Layers:
	-	`sha256:6b3c09bcbd6a79dd8395d4b12ed3ced455bc393996ce768a7e076eea71678be6`  
		Last Modified: Wed, 24 Jun 2026 02:23:46 GMT  
		Size: 5.1 MB (5139894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be2654d2bd171eda83c04982013c1636abe9a8a9117472c56992949ea3fbd25`  
		Last Modified: Wed, 24 Jun 2026 02:23:46 GMT  
		Size: 14.5 KB (14538 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:28a3c805f737f7ec24afd9a69d8e93cf2cba2cea6453b999f5ef6c27d5d86088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237669325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126c795529d4ff1048dc6ccb930259aa52e647e0b3f189d3c5fdcdeeafaab1cc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:52:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:52:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:52:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:52:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:59:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:59:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:59:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9eccbe8efe873f5e82d4f82436ab3eea1a1008796fde4ec310dd8842d87b4e5`  
		Last Modified: Wed, 24 Jun 2026 07:55:17 GMT  
		Size: 133.1 MB (133110623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eca61c1851638343035b0b9f9970ea9830901c9aa2dadcfff4b04fc0408a32d`  
		Last Modified: Wed, 24 Jun 2026 08:00:01 GMT  
		Size: 72.5 MB (72476081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ae2e34ee920917e2d58f02c2d1f04aa68794ef27947da6b81c5afdcad283`  
		Last Modified: Wed, 24 Jun 2026 07:59:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbb2536f590b596aa2c4ab4510c32bfde94492de1e2da5818d647a907b86058e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8614708d0373ee6c8a3908f8f6af4d4d7b4405ca17966ef24ac90c76de2df9cd`

```dockerfile
```

-	Layers:
	-	`sha256:16cfe03fe37b9493af31377f62500726c041f784de330f1cc18a83a3a12ca6ab`  
		Last Modified: Wed, 24 Jun 2026 07:59:59 GMT  
		Size: 5.1 MB (5138058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5643a7cb07214fddfc0fdfb2970defef865013aa2bb67a8c825e2848d4718535`  
		Last Modified: Wed, 24 Jun 2026 07:59:58 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ba8857993fdc4f26914cab4144f34fa14e3dade356a0868506a8c4c44bc1b350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218999296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b084113a3440f1d9e2197e22fcbd721c868b1cdaf2f63ff90509f8e77b4102a6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:10:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:10:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:10:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:10:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:10:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:10:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:10:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afb9c6c476db4f4ef04ae244d61d4d3c9cc2b306471086366d8f73a09019af`  
		Last Modified: Wed, 24 Jun 2026 04:10:45 GMT  
		Size: 126.7 MB (126652577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0de28e21c243a3cc43999661c44f4bafdeefdd78dd611c7d3a1ecc4c20c4f`  
		Last Modified: Wed, 24 Jun 2026 04:10:44 GMT  
		Size: 65.5 MB (65452489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e95e8c8891d08427abf3401d61453562be7c8d4e0b0ec51071e551c29b0ec9`  
		Last Modified: Wed, 24 Jun 2026 04:10:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24b82ac7a559eafcb39d80c13b4c1cd20ce2477c02698bb567c7fd30091f3149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeaf757eac82055c635161defa910f444a97a9ac67aa70631b48afb67f292c1`

```dockerfile
```

-	Layers:
	-	`sha256:78c752b67ba1aa1bc0e85fea987a0fcbe5520f00875737f5d13bdfca54e33102`  
		Last Modified: Wed, 24 Jun 2026 04:10:42 GMT  
		Size: 5.1 MB (5124840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f905d158f56b861767089b754031c5f1c4169721acb6bb2d9e4f669f843e14b9`  
		Last Modified: Wed, 24 Jun 2026 04:10:41 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
