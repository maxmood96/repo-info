## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:1f450509b514fbd23bcc2858ec138e24a0600f1c37d7d0eae45ef542654a31c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7133e5515bf6a03534b9effade90cf514767a657b0e2f61873efd639edf2b6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275573518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6b213f31f2868a94aba0d8c8baf3a3799e7c03a10fd46a3273a278cc279260`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84056db697da37a3615b25ce1fbfd9907eed4795489c07225cfa03a6c76bf3`  
		Last Modified: Tue, 23 Jul 2024 07:13:54 GMT  
		Size: 145.5 MB (145504811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e17724f744f4cb6158d3f5ff4f8540aaace120a8b38a72c5057545c6bc46e5f`  
		Last Modified: Tue, 23 Jul 2024 07:13:53 GMT  
		Size: 80.5 MB (80513987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c764a58e5efaf9be35ee9170a22a178bbe71fbae66c9239ba2126a48380b3b2`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6190a54c5f295bbec42b2012260fe16f40cdd87a17d5c547c9c36ef9f3bbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665301e45142fd0d02784e13eee6631939f35e33ec2e91c814d3871d770c34f9`

```dockerfile
```

-	Layers:
	-	`sha256:36594dbb83b6a3be9d1becb51929d6a188adf0a93fcf950d277dc8556cf6db2b`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf6da4b27f07f9195ed70122c49ffe8191edb24fbba8c4f2edd9d960981ece5`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d1dd2c6f92e8ed05c2cd9e97fafa0601427000a7c1cdd0aa857e3e8883c1969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272155249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e92cb69e9f752de6101a0d5cf74d35c9a3063d8e3b4530b4ab463f211b699c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fea38de30260d43f422f9683e44a016798cadec414b573bf08a1cf8b3a729f2`  
		Last Modified: Tue, 02 Jul 2024 09:19:19 GMT  
		Size: 142.3 MB (142304084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87279cf8c58e00a8b57b707b9e7bfed15a1354ccf6ba76710d60fdcbf9bf06e`  
		Last Modified: Tue, 02 Jul 2024 09:23:14 GMT  
		Size: 80.3 MB (80262072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc549108e75c5b8394f512769f94cbb177792ed46234cb98b2adc77ec3f9d535`  
		Last Modified: Tue, 02 Jul 2024 09:23:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0ef18ffe527f0e7bd60cb1bb62fc46d134e5da2882d77ded9244fbcf41f6d33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc6a418c42834504c0c68b691c159f6bb6150bc3402dfa9ed3c7f1f594c913`

```dockerfile
```

-	Layers:
	-	`sha256:133f8d73a5acab4b4cb345e136f939fbc6b8243d1c838dcb035afeedef270e51`  
		Last Modified: Tue, 02 Jul 2024 09:23:12 GMT  
		Size: 7.0 MB (6966348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd999fc6b85af2e9f9ca8f26b11dd07fc0a37d3d3fabdb696c79d78993644d5b`  
		Last Modified: Tue, 02 Jul 2024 09:23:12 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
