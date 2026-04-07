## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:3ade6efc64bf03cf245ca011c798986c01033fa717c93a7e74490001b13ffaf0
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
$ docker pull clojure@sha256:8baea2e09c4afaa1dff2dc8cf6bde775c24f7738f2c628b5d4ef3bb60ae9136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243745693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2828f10991c64fd181d32f82b5b9671cdd334f72730443875e91879c4c813d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:53 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb099f9faa969a2c5dd14ef86cb1e3876d080c240a574fff8af8e5d0102dc4b1`  
		Last Modified: Tue, 07 Apr 2026 03:14:30 GMT  
		Size: 145.8 MB (145806933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18e6cf36030888bde2b15be9175dd2b559bfad0655e751e8cab8aa6cec32192`  
		Last Modified: Tue, 07 Apr 2026 03:14:28 GMT  
		Size: 69.7 MB (69701783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb854388ff7b489471a3c101f8245366f85c090153bdf226ed7f806ee046aa0`  
		Last Modified: Tue, 07 Apr 2026 03:14:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddc7f7dd913bc2fc5b76b2e47aa911a901ca9d548f1119dedd800ac2ec2815c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f560daabb02b6c04d3a38c756117dfcf40083da33b6a655e9f4157f2e395dc53`

```dockerfile
```

-	Layers:
	-	`sha256:c1a802c88ad83432000e6380d55bc139fed76cb2b06b57ad060b79c903d83028`  
		Last Modified: Tue, 07 Apr 2026 03:14:26 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc7bfc3646f7d475e1ede424f062858515e1aab3fb2d2cad1e04c6fab1db8516`  
		Last Modified: Tue, 07 Apr 2026 03:14:25 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ab85718cb1afac1fad1fc47694bcd58c1bb18f379c3a2282f340e7712aabc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240305892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4d36e8515313b181220861138692a45e683be3df77f3db77ded3b418b254af`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:24:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:24:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:24:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc6e0cbc2af790fa23a290fe58a67d404e27cee648ea940b94c49e73c1df84`  
		Last Modified: Tue, 07 Apr 2026 03:25:06 GMT  
		Size: 142.5 MB (142500069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a86b6185d9c3f85aca37c8dfd93d3caeb202237bf870771c22ddf76de97e2`  
		Last Modified: Tue, 07 Apr 2026 03:25:04 GMT  
		Size: 69.7 MB (69689012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d122e6d3cc19cc4f448722cb262c10708ae073912fa6938a08e1f5bc807b96`  
		Last Modified: Tue, 07 Apr 2026 03:25:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fea76cf4d11ae3978d16d83b22ffd053d3593d697b4d618bf00c628bcb4da2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff69430b66874c2d3a794c013de3e617abd50439ae9fbb147ec2eec7afed29`

```dockerfile
```

-	Layers:
	-	`sha256:65a7b1d91cc94bff4c736b491b7c37317c1ad2c2b42844e4e7f4b92a7ff1a1ac`  
		Last Modified: Tue, 07 Apr 2026 03:25:01 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36e72fd3b0997199b87f5e197bc3f1d8d08536bf8742b964535f99279d5ccae`  
		Last Modified: Tue, 07 Apr 2026 03:25:01 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b0dede37804225251f78c9a26d7647cee573a9795b92fc18c320a0303b33363e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240609197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01662af727b23af2a814ce5dc760e4eee378bb276b7aad495c228e1fb7cea4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:15:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:15:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:20:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:20:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:20:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecbf7ecf5689b9ec9a2fb7833196c9e479474539bbea61e477b10fa3c1a715`  
		Last Modified: Tue, 17 Mar 2026 18:17:05 GMT  
		Size: 133.0 MB (132996700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dfbb26150907a453339039291be9977b5a76c23bc9e9288aa29ffc9834a54c`  
		Last Modified: Tue, 17 Mar 2026 18:21:26 GMT  
		Size: 75.5 MB (75533485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf69382494015a17d52c23dc57652e8a188d807e8e0620e0fc5d7ab686b14dc`  
		Last Modified: Tue, 17 Mar 2026 18:21:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f989c33a0cade7158ce771b726f8fd4584a74325641a17ac7b70ed882692ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915430a901b4b283042558aa2b16269f4f3876421611e6ccc7922a4b006bca26`

```dockerfile
```

-	Layers:
	-	`sha256:4d7e9716ac9887c7f657424b16317b0514a5da178e6afc1dd49dbed7fd0ba5b5`  
		Last Modified: Tue, 17 Mar 2026 18:21:24 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73663b4ff4d61aeeee7439f41e567f2e82889d1cd65c5bf25466c2b201a8b0a6`  
		Last Modified: Tue, 17 Mar 2026 18:21:23 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe3514d027d4e1e8a3a0c28fd4bf457693c3ed910193f0a769de42c67925f239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221968099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71905062eeb99cfc2de3036e7d71a343eb7704f8263c6084ef2de23a110696`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:40:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e385f726bab54d70ecc51bad16d60533bc9b6d182b632879bc3c86a7da9d89`  
		Last Modified: Tue, 07 Apr 2026 05:39:56 GMT  
		Size: 126.6 MB (126562190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7eb79f05f084698548b1b10f8a4ecd434f5d5c2821d46998b074a17e5361b`  
		Last Modified: Tue, 07 Apr 2026 05:40:52 GMT  
		Size: 68.5 MB (68513630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798fabeb47c2a9d9c1c3aba63ff4b02fb5c5a8c4f4647e4d1c32976bc74f9bb1`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:055c94a0a784c1ce4da1c215c168b0e7dbd439080b5cdb1040ef90d8f6722471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5dd4c10e0a745b5106033f547ee128b2cbbf98fc9b1d5609018ea3e92fabb`

```dockerfile
```

-	Layers:
	-	`sha256:ca57aaaf7510edcc5983c73d136f36cc142a1ca2b96b326a045da3d8bcc78de7`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4aabab24801f056ffc696b5bf463701ed8c1d02bd704212a6b3800931971d6`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
