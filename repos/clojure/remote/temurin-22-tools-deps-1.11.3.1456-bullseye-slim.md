## `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:8065136c6035dea68938048ff48a555288abc68cb8a86042cc5c7ff624ac8c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ee3d7dfa5856d21f26faacad8d534c7f321d46e005e3006b7a80dc99e2eebb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246570583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfab1ded0ee3d7d60d47d3aec1ec366479a67eff4f27e28f2f561500b5e57dd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92922d502945f8ccbb3c5ecf0aa43657388aca78261025ee5da6f44dbf8b3874`  
		Last Modified: Wed, 29 May 2024 19:59:26 GMT  
		Size: 156.7 MB (156715503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e453dab1022daad57065921301d09403dc2c65183e6791457e8a872e1e18b1f`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 58.4 MB (58420099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708075673b27ce0c51745c9c81c6bf46c31320edc9222100a4d95b60db354b22`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f04634ee5f0380798b80ee3067f5054610a24e33b8c1a3a2f8b1840d328bb7c`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbdc1ab026bc5777b49d55864e3fbf6061c32eb9f3c278317cca5f585977b002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09157ee44823296384792b99b24260d39fbfe589e70e87cf77f6c16c1a5ab31`

```dockerfile
```

-	Layers:
	-	`sha256:a716bb4fdb28bf3a1178da763a53e69af5f622926ea55c9a97d074119517ed7d`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 4.9 MB (4909228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e66384f6a88444aece8df4b9057ef05396d35e6c14d663c4bb804c84f42286`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18f69262d19b3d75a8a995f5955ea5015bb58989e8f2d579e62c28edad4c16fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243365979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f48f9d091fd6cdc9a13e0b60297d520ac95a8ce29f997348d7ac0f3c5d7bb43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e471be3e11437e97406a772ae65a3e6305a7b5b12bc73656a94efc507c23f007`  
		Last Modified: Thu, 30 May 2024 01:53:41 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a72824eec2c99892a02f846ae7bc588c5ed4719c041a06fdf67176d8b74879d`  
		Last Modified: Thu, 30 May 2024 02:08:47 GMT  
		Size: 58.5 MB (58540024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45391b719a6e3de4ec22d3a5b0bf7ed642b463226f311fb8b84ba0690485c50`  
		Last Modified: Thu, 30 May 2024 02:08:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c5da686abbbd9971d252df7bcde4ecbf01c66eefaa5fa6dccd1bab2a31527c`  
		Last Modified: Thu, 30 May 2024 02:08:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b5fc24325f2288763569158de1846e5da787d4d73457b4ffe1df6e17d5244a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d03a8bd5f6584be55b686f3265b28e73f4a248fced89786c236e79e33b26f1e`

```dockerfile
```

-	Layers:
	-	`sha256:a4449a102c81619f331c2baf95e8da27ceec70300bc94ed3c2e3959128a4238f`  
		Last Modified: Thu, 30 May 2024 02:08:45 GMT  
		Size: 4.9 MB (4915584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c1b543e7bd4c698f2b71ed6f7c98f6999535848719c76c9aac840dbb8c5391`  
		Last Modified: Thu, 30 May 2024 02:08:45 GMT  
		Size: 16.0 KB (16003 bytes)  
		MIME: application/vnd.in-toto+json
