## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cc11564bc757a7a405513de91eb4a753045b119acefd7f8afd6a5169933bd7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d12488fa86f278ae1b758baf6dacf196f35a3be6c2e050dc2b5839cc427aea10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16bfea681d7942f5ada6730e11786f903feb78e868a3f190c3d84c2e02f8577`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187395b0db78c015e7d301886972f3cf2619cb9c54184751ec46415f784a751`  
		Last Modified: Mon, 09 Jun 2025 19:09:05 GMT  
		Size: 54.7 MB (54716173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1687b5b3ccacf12ec366dd4506fcce78d46d550e5490b84cef2ec6eb2b7759`  
		Last Modified: Mon, 09 Jun 2025 19:09:06 GMT  
		Size: 59.0 MB (59005648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5d175a52e1ec858503698c5f3d4d74b532017d7a2eb864400b9ceb84baafa8`  
		Last Modified: Mon, 09 Jun 2025 19:08:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:daecb4cfb13b20c71363272426e34d34898cf12b714166c5386c65b9cbefda44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac94a86bc379df3009313b46bf6d7baac69283b1f7b8ed1a49eca65a1f29346`

```dockerfile
```

-	Layers:
	-	`sha256:914f978cdc7a2de628fcde6d861b54c9072348803318cd724760b289567b8228`  
		Last Modified: Mon, 09 Jun 2025 18:42:51 GMT  
		Size: 5.4 MB (5431272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff226c10f7c99ca8e28ca07e1859ab2a9e2cc4d755aee88d775a8a3d4dee8ab`  
		Last Modified: Mon, 09 Jun 2025 18:42:52 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dfedba68ba5e4f1978641131c29ab36405cbf189aa37b381e5f5d6593d4495ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141714902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3facf82c64a8197790897b676ce12476f1c2cc5402ff8205a26a86eeec4aa7ad`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a26ea748e01f6fa271cb5c99f02841ad6f2c475c5d2be97781534dee920e77`  
		Last Modified: Tue, 03 Jun 2025 19:23:28 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59dde2c4896f90ce1cf9d2fa6b6b467d61fa7a6605ebec7eb20ce71ae635b0b`  
		Last Modified: Mon, 09 Jun 2025 17:34:26 GMT  
		Size: 59.1 MB (59137504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126fff26562b1d7507a6c0045069b13c5baa3663c34317e96a305bcd55b18aa6`  
		Last Modified: Mon, 09 Jun 2025 17:34:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:caf2102d0dc7b7d522ce4aad492fb7e98f1248ce9b1281687bd735f467435678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cc93b2b27aebb5569ad7edb9555bbce38ee81929ba389042110724750ca02`

```dockerfile
```

-	Layers:
	-	`sha256:4063d6ddedb286cf6a9c485a39f733d3b3cb334663c05a99ecf3b20dfc769fd7`  
		Last Modified: Mon, 09 Jun 2025 18:42:57 GMT  
		Size: 5.4 MB (5437702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eac334417ef7bc563113aba790930bd4448261242756b30786d2ae370e887a3`  
		Last Modified: Mon, 09 Jun 2025 18:42:59 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
