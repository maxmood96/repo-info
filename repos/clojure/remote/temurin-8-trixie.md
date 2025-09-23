## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:3e8a03323d15ff1952870a2cddc2c5f39881d1ef20ffe60305b1c9ccba1e9cfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:81c4c1c20c03ef4054825a7a1ebc42e106f94a8049d8ff5057d9b28a80ff694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189543734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976678dce012a31b81bb62f5080e6e83a9cecf256062057b8c36e181d48f58ee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca61f957cca520b2c1f12dfab84d435b277af206300460064f51815e603a4d7`  
		Last Modified: Mon, 22 Sep 2025 23:45:15 GMT  
		Size: 54.7 MB (54731308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c76530f5306712d3971b2d10e682127f9e070585356bdd707c5e11ac7e28fe`  
		Last Modified: Mon, 22 Sep 2025 23:45:05 GMT  
		Size: 85.5 MB (85532249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abce9d0b18a50fefa002550696f476d0ea2130089c9f03ec7ebf2c15d79219a`  
		Last Modified: Mon, 22 Sep 2025 23:44:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:800399b97eb2514c9224ae63661206b8ccb343e1d119b1ca2e03304726e2933d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654497b972b9ac2d1398cc34c7960b3bdcb4ff7d7d09b48b63beb750bd3f8b15`

```dockerfile
```

-	Layers:
	-	`sha256:00a4ffde0da547771c15ff6e336be27ab89004898710700abad5a68534a33221`  
		Last Modified: Tue, 23 Sep 2025 00:47:51 GMT  
		Size: 7.6 MB (7588455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d22892c2413afd8ca5d4cafc829dbffa1bd19e8de4c3cd023876e0232050fffc`  
		Last Modified: Tue, 23 Sep 2025 00:47:52 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26b63d5afacdeba0c831d3802472e94a1e59e41b1417699be16869a9ff810fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188838694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc4fdbbf3d231b60fe1f87998e7f914cefc3a0ef5d81d7bab653d9fa4ab8e6c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e571731e535f2f07758942c1cd72f53b0e395cab8a096332eabf799107d4ed43`  
		Last Modified: Mon, 22 Sep 2025 22:17:04 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914883374016209928b07db12881298883762d3881e56c133b83890d1cfbec5e`  
		Last Modified: Mon, 22 Sep 2025 22:17:23 GMT  
		Size: 85.4 MB (85358695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f18861e17f847099c872ec2494934197ada7537ff76137fb46319af51e4cd63`  
		Last Modified: Mon, 22 Sep 2025 22:17:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3bd577f33745f3a597df2ff393a24d593f346075e9f629159f585632fa5452e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ef3d9492a41091b66be92ffa11a2a287d77c93eca057d39daa3c87cb67f94a`

```dockerfile
```

-	Layers:
	-	`sha256:1b0797787fe1ee7026f23803c017f36875df626cedf0b1ebe32c343c4ba991a1`  
		Last Modified: Tue, 23 Sep 2025 00:47:58 GMT  
		Size: 7.6 MB (7596183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e7171bfa2a2046fa51b546cd6f44883ccdd0c302f918634ec9f121038e67ee`  
		Last Modified: Tue, 23 Sep 2025 00:47:59 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8bdaf19bb281920887095e8fb2c06978aa691f4d12c07704d8645a9822f10324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196224771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c15c45f8e5cf8e4f91f6dfe7d5e38ce27d9d20fbf2eebb4edf11a0336f571d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc46708712e2739dd223f5a5084a3758b7e54dc9a68ef7ee76603b0b823ed7`  
		Last Modified: Fri, 12 Sep 2025 23:49:00 GMT  
		Size: 52.2 MB (52165393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0d433ae36d1b4773da94783e1e791e0208fa8b41ab296e56ed3cd21dcca7fb`  
		Last Modified: Mon, 22 Sep 2025 22:43:12 GMT  
		Size: 91.0 MB (90954299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66800a22f6da5229469f841a67c38765fd544b0b37ac87816a4c8a520c6c8ec0`  
		Last Modified: Mon, 22 Sep 2025 22:42:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dd8bc0cf115d76873e422a912d12882dc657146080e0b1138b798ea0f9de0ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51c2ce898e32fe91d1f2f8f548ebcb1d8b302f2f55ebf91752996a453ac20fd`

```dockerfile
```

-	Layers:
	-	`sha256:9a9991e2cac6c5abc18be48ec02b08627b209b77eb4fa3fc512ca10f75164b6c`  
		Last Modified: Tue, 23 Sep 2025 00:48:05 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b53bec88d052d0dc1232021ec53596c27828d0c9f10e334db34597c6ef2adeb`  
		Last Modified: Tue, 23 Sep 2025 00:48:06 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
