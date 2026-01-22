## `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:6c9d644e5f21c147ec2e771b225986e83c939442cc7b68ae7955cce7c0fd5a83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bed06ebcf8aa6106e2a5acdf70d1164a7402f3bc528ed8f88b085610defa538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268161946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa06158d9e74c5de1203d9752542e0eb855cf26a8da7d0b00f5a58da0354f0bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:55:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:55:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:55:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:55:04 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:55:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:55:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:55:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:55:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:55:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ae4a115b226ff332aefcf971a5bbf7be9f26f9fa2dd9b4bd7567e8c907216a`  
		Last Modified: Sat, 17 Jan 2026 12:54:34 GMT  
		Size: 144.8 MB (144847942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a43e24dabbb23b799cb278be0662ec25bfa4240292021d00bc27d09e5dd4c05`  
		Last Modified: Fri, 16 Jan 2026 01:55:54 GMT  
		Size: 69.6 MB (69556516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f902e405bdb1bfc028b39b50bebea379110764ed25007e7f6445a5e877761e`  
		Last Modified: Fri, 16 Jan 2026 01:55:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48df432cb48cb844642ad4415ce5b2402de7e3e9da724789fd92d502200080a`  
		Last Modified: Fri, 16 Jan 2026 01:55:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ee8abefe7c310a0daecc52c51e4cc21639f5839723e3601c19f3b92f1d6e46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3669be36e0642148d99e681a37657f76dba246ce3dd40558e3d5c18add305446`

```dockerfile
```

-	Layers:
	-	`sha256:e34a503ce40fb5afe347349cede13e5458ab41e0d71c90f2446c6f473d42f79b`  
		Last Modified: Fri, 16 Jan 2026 01:55:37 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4422a2d26a440f313f6b4774abd1240bbcf1a761756e33f62c7de698efefbcb2`  
		Last Modified: Fri, 16 Jan 2026 04:41:00 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d23c13bca32a660af9af3ff0cfb556ab53406b06e14441101fac329e0ca1b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265625575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc88ad88bd5d28f0366618998149c54df128b767f3385231f48f4008d715105`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:56:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:56:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:56:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:56:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:56:22 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:59:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:59:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:59:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:59:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:59:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570bc4cbcbb0d0939d17ea76364760f5ba4a88c7d52dd417e07658664986905`  
		Last Modified: Fri, 16 Jan 2026 12:46:50 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5742b13f294bcb793e133ace2c98b47f0dc0f85492448d13ab2c969f7dae7`  
		Last Modified: Fri, 16 Jan 2026 01:59:28 GMT  
		Size: 69.7 MB (69686835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5a70f661029524e14c2f0da8a8b6a5e574b2f6881896a49593288de878c7db`  
		Last Modified: Fri, 16 Jan 2026 01:59:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528479ad7ea0ced270d5d045a4935b21bca385a549a382476bdfcfd61bb11d8b`  
		Last Modified: Fri, 16 Jan 2026 01:59:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e2e3150fb6cd310243e0df57408490f214dff98347070b0f7eb7ff468f114df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb2457e17c0b69450d32b6643122772477156700528a683501e2a7f20f502a7`

```dockerfile
```

-	Layers:
	-	`sha256:f81fd2db2ea0eace4cd48ed7028c3e4d6f1215c7b997fa4553af3b2d41d46c79`  
		Last Modified: Fri, 16 Jan 2026 01:59:27 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff62a68466ee3d9f0c539a9de4065d2e4171d8684c6bb6639d51d15935accc0`  
		Last Modified: Fri, 16 Jan 2026 01:59:26 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
