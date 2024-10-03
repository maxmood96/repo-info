## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:8fc340a9f3c3333f826de932529108c8bba79a430286648e72a359946d18f1ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:b042f5729edfd7cdd8b891690ed13280423ebf3b2a6aa7b4f158167dfa4556d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eee936639e54cf02b884eae88a9a20fe7b48328a5ed1714f5d59f1e6fa4e0d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79012ff928e60e39df52b7c64c9501df5710086be94812dc9a25f5e5b5b94a1`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 165.3 MB (165267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f47be6c65eec3a4a8570f907646355223d6c11796869289cae9bf28b1d64986`  
		Last Modified: Thu, 03 Oct 2024 19:00:56 GMT  
		Size: 80.9 MB (80928268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54de2d03a38a4dca7edd069df72cfe816dcbefe3e743a73e74a02a79785489b`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f1e0c13dc04687639f7a7f245b4fb52a54290c14bf2de799192d3e3ee54b03`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:cc593f2fa60b58709d4073762837e95969745fc9b3aff68e986edc74b93373dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b12a358e6f8db57c30d276385b834081220aea12f38884862e3778ae1d6114b`

```dockerfile
```

-	Layers:
	-	`sha256:b94f1c032c7ec01f0ba850a2b82035ed2f0ada0d8365a1d76a5740640d7ce220`  
		Last Modified: Thu, 03 Oct 2024 19:00:54 GMT  
		Size: 7.2 MB (7162323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993170918376f44dbb09065be2fb87234738cda7d976da8fd417580989d3bce9`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 16.1 KB (16129 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f04ff5859e204e6eaf8a8001f5ea0f29465cc07b065d4be256e5ec1d9bdfca88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293629245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5ac0ea4e77ea179a6900e1595c20ca1c0e8d94e14a2acb4753399d7ff36b3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
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
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd4646320d386687be33160a1cb9db47c711fe0f46f942c4f39ee5d54f71bf8`  
		Last Modified: Thu, 03 Oct 2024 19:00:47 GMT  
		Size: 163.3 MB (163252821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d85df5626297274d3f42fdda7c9d67b9a1fbe492d92ed065dafc1493257b33`  
		Last Modified: Thu, 03 Oct 2024 19:06:45 GMT  
		Size: 80.8 MB (80790499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5a3c25e2a1726504a7e6edf479c705efcc15d47cb0c5073671f9abd5ea7949`  
		Last Modified: Thu, 03 Oct 2024 19:06:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d1f8cae691942a7f92337b46da5206fde855aecafdb9d786b1c3c612e4e49`  
		Last Modified: Thu, 03 Oct 2024 19:06:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8abba181100cb4d6511c7dccc36290452fb8f981b31016d082ed1e66d87f14b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebba8393c83897b148ff4a7113664be3e5121840d6fa4c09fcb8e7375a4766e7`

```dockerfile
```

-	Layers:
	-	`sha256:827813721d6a2ce2e750753fb6e1a8d7d0d169a8f82d485d1cb1617ab41fe329`  
		Last Modified: Thu, 03 Oct 2024 19:06:43 GMT  
		Size: 7.2 MB (7167493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb344d1f69f87657ca14f1d606ceabe4341d3954e1b391f4f9ab8dd075d1a2e9`  
		Last Modified: Thu, 03 Oct 2024 19:06:42 GMT  
		Size: 16.3 KB (16257 bytes)  
		MIME: application/vnd.in-toto+json
