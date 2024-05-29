## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:abc0dce9ad37835eb6aa01131cb296e61efd0d8956917ab33f550c87d2ca95de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d5375b5575b495a316b8d22b81f9b03247a66fa6d8fb0f43aa03d3f3d9abfd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234950418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01459fb636959c9a73cdbc563cbc4359ca222b01dd54a1d16ed3a6bcbbdeaff`
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
	-	`sha256:de5de861d2b66ce5fecb8d8cfca530ea75992f9daa0962cd262a6188b0708007`  
		Last Modified: Wed, 29 May 2024 19:57:15 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a282f5177d1a49c64a480505aea42412218436def75c756efb5f4ca947b3b8`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 58.4 MB (58420398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66863c2f6e08f6edee4b9d98d5a8b3687d5c21296231649f190bfffb65c08fb`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89bd60a563876aea42876226d4d34b757f82d7effccdd1296916cf61796c497`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3300940ee4d2a3543f2ddd4478ed923e03574626d447a6f4d36d3900f8f2af05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3df38f2bbb14ed538500cc8442e281db3948858d49dbe0bb7d83d5c1c0c9587`

```dockerfile
```

-	Layers:
	-	`sha256:2444f4b6dca65a6f205d8ed4c1d32c71a7530f811931d32b409df7c7aaec0282`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 4.9 MB (4909234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1d291ef982420394e55b18875087cc60bb4d4d71c6a1a1068871406cc7318e`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:094035d96fbdfdae0e877fdf7f104289e4422819b5ea36c5be2e4e7c5edd864a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232728118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517076eb983f9ee5f6dfe084fe7ca145ec7de1f98a8220d3564edf9270e07b05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:55:44 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:57:45 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:57:45 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:57:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:57:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:57:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:57:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:57:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf072d6312eeb8d6d05dc50f44eccfa94ca9ae5a08d2b299b845776b87f175a`  
		Last Modified: Tue, 28 May 2024 20:15:28 GMT  
		Size: 143.9 MB (143891870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b948b2b1d5095883ac552af06b8b9b937e1fe64cb5fa4b24477e72320e81c8d8`  
		Last Modified: Tue, 28 May 2024 20:17:11 GMT  
		Size: 58.7 MB (58748326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806f85dd8f866b9df6f6cfd16310786f803f36b46d2e19bc28ad480d4d85a8af`  
		Last Modified: Tue, 28 May 2024 20:17:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be62f08a3ce83443a8f8dc7b92d88231436cb316a8361b3b7d0b399ad04bd7`  
		Last Modified: Tue, 28 May 2024 20:17:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
