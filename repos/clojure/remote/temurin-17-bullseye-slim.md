## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:8bbc69793e495e2bb543bf090c36230b6d71955635db33c7b4de3e01bc867cff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

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

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba024209799cafe94020111ebbba64d4f622bbd3ae596838c607ae53f583ae90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232520766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493717925b8140c684e5eb378198a87bb9ee8048d1398d359a7e2c3f428fd781`
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
	-	`sha256:f63f4ee817206835406fa1b0460fced3be1020c767f6ffcbfc59d1cd869af272`  
		Last Modified: Wed, 29 May 2024 21:41:18 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d67400a264fac44f2035d924070c06671472ec03c2c7e8dc735dba7547ed221`  
		Last Modified: Wed, 29 May 2024 21:46:07 GMT  
		Size: 58.5 MB (58540036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73ed7952b8f3ce9cc07159c6f359d8a156f951a5f864191530ce731ae1d44e`  
		Last Modified: Wed, 29 May 2024 21:46:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c1e63155ad57bf029152b2ef9233dd849eea152b83a30258a17f9e76c20523`  
		Last Modified: Wed, 29 May 2024 21:46:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:909f0bcb0abe6f5aab35cdcbfa46f3d571fb18bdeed01392fdc324d786bb7d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae71be6d9368cbb0d4417314a1b5f1e0e32438e2fbef2f950806526eaf94c06d`

```dockerfile
```

-	Layers:
	-	`sha256:d2c6c06026b275bc7c9eef006285b3a33d6c06abe4d400e0d4e8b8ba26a4468b`  
		Last Modified: Wed, 29 May 2024 21:46:06 GMT  
		Size: 4.9 MB (4915590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525d335a1cd0312a61469b7f94d059f3260bdce96079592ae69719693f2d4480`  
		Last Modified: Wed, 29 May 2024 21:46:05 GMT  
		Size: 16.0 KB (16003 bytes)  
		MIME: application/vnd.in-toto+json
