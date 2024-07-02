## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:14329232a1362f8dd2ce1a1ace7e76eddb8fa36c4f275dd210f0844b11504aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ed213e53a6641772bd5d614dc4fca773b303e73dfe7e07ebf2cbea314bfcef32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275571171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae49813d67fdc31bf11a68edc475d8db26d458f151f373f9a1125c6323ebaea`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d21d9cdeda13986276d3db32d0e364b9dc845bdb658b181e4a28994091f60fc`  
		Last Modified: Tue, 02 Jul 2024 07:07:10 GMT  
		Size: 145.5 MB (145504804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83108fb65a1423a79054ac41708bc343aeef59a9b2d36b4e057d465aa96420d`  
		Last Modified: Tue, 02 Jul 2024 07:07:08 GMT  
		Size: 80.5 MB (80511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ed0a5bc8cf05e3054c22b53098b3cdcdb748a34c09c64ac14a9265f311d3e9`  
		Last Modified: Tue, 02 Jul 2024 07:07:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:487fdce841f06707d385fd79d6f785e09d06d58f81a19d30cd38a9bdd79c6d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6973824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4210ae6d0090c3a0987056fa8f78fa177e6dd683ec4fbe0044d6c3ec1daf25e9`

```dockerfile
```

-	Layers:
	-	`sha256:786d04813c12d47bc3570a8f528dfdb1cc1fd2bf28af2b83283faee91c15cdfa`  
		Last Modified: Tue, 02 Jul 2024 07:07:06 GMT  
		Size: 7.0 MB (6959961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8886a2ca4e9080d5043620919f33c0bbfb7a91193075a11325d0181e8ce0ee`  
		Last Modified: Tue, 02 Jul 2024 07:07:06 GMT  
		Size: 13.9 KB (13863 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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
