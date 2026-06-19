## `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:4de7041ebb9256ddccaa64a1ce84200c8c45231a3d626d334ec42a2d5faf017e
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

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ac728c411c7bc60e1d9d9af18fc0fd6917ee5ebf0100a2196f18f6e26808ba77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284795148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252163a66c6d79627a6fb65431d631d1aae904a3f86df36d3763d0f404e990b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764ed8c437ed47d5c9d3cb421b8be1e8f110c68492cc940f000e47a987462e9f`  
		Last Modified: Fri, 19 Jun 2026 02:19:18 GMT  
		Size: 158.2 MB (158166941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34969f75d26922feb3f1ee962c171dfc5f52677e719d650702cc675fd9f8f032`  
		Last Modified: Fri, 19 Jun 2026 02:19:16 GMT  
		Size: 78.1 MB (78125124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2647e0801cf3fe02a10e3e384c66e814bbf8fcb722cb45ed31852f836f93`  
		Last Modified: Fri, 19 Jun 2026 02:19:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36f80f4e268b7b118eb2072fc1e212625c0c95dd95924d69b05d85b7ab2675`  
		Last Modified: Fri, 19 Jun 2026 02:19:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ddc37f7cabed690f68d4bd3b9fae7886f5392c6bf8304fa8ffa3e22e00350728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5e8ca6a8f3767c6be2b72aa4362b8d07072d07291682bc379be14f33d6686b`

```dockerfile
```

-	Layers:
	-	`sha256:489946a27b2ff235050dc52540e53ed5adfbc5d420332278889d6292ab5f6f3e`  
		Last Modified: Fri, 19 Jun 2026 02:19:14 GMT  
		Size: 7.4 MB (7378670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f5eed3af8db1adc1de088574c6e3697196d54408ff641559d885cc567b23a9`  
		Last Modified: Fri, 19 Jun 2026 02:19:13 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:515419079d07f558374d170aecce4c0efec01f9c08dd689bb26d8ec2ebf9b074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282979995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff6ecb8132b988cb1c989d86f06079fa88c02c670e465255388c1546713397`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:10 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb63de71613b0ee95a71b2390ea662e991a4523125ce8fd3b7f353b29e010096`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 156.5 MB (156461328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819bf8284cd8ceb753011e77104ef6689a179aceffe50f57a805f4719b5963f8`  
		Last Modified: Fri, 19 Jun 2026 02:19:47 GMT  
		Size: 78.1 MB (78128609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66c53faf202016b0b9f3b4df2a9f7fb30902b1bf053beb26e29c67a30f370a8`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0e1dc3d68570551a6def79bc2da0f7d4fab8b87423470bbaeacaaa93838898`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fee7fe987f6716b91d32035a7cc757e6839ee53713de3d3eb128854a3c4b8809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd776183cc81fbe894faa5d28af5028e47433d43ce2e473426ad0409a8e2a81`

```dockerfile
```

-	Layers:
	-	`sha256:a710120257ae231b1dc8dcd53f19fe7e228f6b3474c4f05311e979827dc26cea`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 7.4 MB (7384457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d0275f245a92a6ed457169eee3367fe6e78f35b799e46537f8e3f08e9b21de`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5790516c33246f0ae3f87ac19bb2dd56cc8483a5c34898dac31789c6c7497510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294649537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba940732e6e5be1e719ae447a503097f17c0f0caa3e6fe85107530c7281a00eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:52:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:52:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:52:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:52:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:52:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:51:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:51:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2baefaed51aa669676a6ca72a1976a52e2ef31d6ede3f6e16283490f461501`  
		Last Modified: Tue, 16 Jun 2026 23:55:52 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76d4606a4fdf30a370796d0ae5ce1d68f7eb31023418b1bdc61dec65a42fb9`  
		Last Modified: Fri, 19 Jun 2026 02:51:49 GMT  
		Size: 84.0 MB (83958581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437237bf82753108a524dc96421224eefb13579517ad60befe7f4d018c188a6`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b24fb6e9645776f5efc2d1cc8924ab2688b027e5cb7462b8cb788c684c07a5`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2ff0cd7d870f50916842f6674bbd42fbc4c6dec1aaed3a85aab9b6a09790502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c409d19986f62cdcd358db789918961840d46e63839414e7f665278ff9e2fc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d428336e5aee0054ab23ea93695fc1fc8b8ed56f6eec6f8a5cb688224725899d`  
		Last Modified: Fri, 19 Jun 2026 02:51:46 GMT  
		Size: 7.4 MB (7383898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ea0761faa926ec3409fd6569ce404a70ceab89e92922da36fc19a794f97029`  
		Last Modified: Fri, 19 Jun 2026 02:51:46 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:db187308878735259139201c24a7701439a99d88c5b9cbcda4c6cc99292ab1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271480110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df5a16044854cd676bd9bb8c2449959e3f1526b82745a45433f3e707b2d8bee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:36:10 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f3439d92caf07670440a960bb879707c16dc5e881fbc688c4e1a643175e72b`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 147.4 MB (147388366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b725c67439d0a7c5a177afc011e08bf5b3f71366b0f05785fa067eeb2ac1be0`  
		Last Modified: Fri, 19 Jun 2026 02:20:35 GMT  
		Size: 76.9 MB (76929207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451226aff33c9198bd7b5b4cf659de5ccc89cdc6c6b10605251e6c1058fe6533`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6849a0ddc42c6660f680465fbdd561f409dca81e0f2e3abae45d99ff65eb4ba8`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f565b66c527c62d56c020ed262757069522c2b1f76da43316c52f97ad850ab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5baf26e809df7a803fe98eeda9a1227123d6ed41e9f35e42e5e16e61f22faa8e`

```dockerfile
```

-	Layers:
	-	`sha256:9b8e956bfe957e002f6f9952213da75cd470b0dcf18f9ec0c4fbd3461d4159d5`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 7.4 MB (7369989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354dc17860e46c3b9ae84d74b750caf000719c3e48ca9b8035290fb1c99f565e`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
