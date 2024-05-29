## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:20bbd13e23f84279a4503334e241509eb351e71cd7c4443f673c4ced9d084725
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:281dc8f4e23cc448e893e20195b2c240e5be5f96b2c9ef60aa5f0b7f21b809e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243573706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff8152e5fb96f8e726bc9b4ec58d6ebaf2768c1086aca1795ec525b1ef6e5e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:03:07 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:03:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:05:03 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:05:03 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:05:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:05:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:05:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:05:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a13a65c57016b28359f586eff3a4b25400f9c7f0f0debe3ae646a1af81eced9`  
		Last Modified: Tue, 28 May 2024 20:22:33 GMT  
		Size: 154.7 MB (154737731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacfee50a6bf727307a8d7c98e2e8555c7f4be08cb67af8c3050740895dc6482`  
		Last Modified: Tue, 28 May 2024 20:23:55 GMT  
		Size: 58.7 MB (58748051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf2a36a01b5badd8ac2ecaee096735d7f6bc92f263386a51641952492ed26df`  
		Last Modified: Tue, 28 May 2024 20:23:49 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2149848655306f415d5a85b92d5f5a1d8815ed6d292bb3ffa949944f025094c9`  
		Last Modified: Tue, 28 May 2024 20:23:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
