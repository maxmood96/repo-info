## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:9de2134e6fea7007f1606bbc16ec6e1eed2c1fea1d37c64abc3ccca58908e52f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:b43f3658dfb5886773f172e7c84463f53d9aa82a15b751a8b4c5356e88937226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294790875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecd8b3398c3c4aa6f4b45c16db60006610fb46df0a79e75de8e639fc6454ec3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842d7d6b0c6dac7c24a8e4aaad0151d3b693cd30df69e4f0e6c506cfe73f205`  
		Last Modified: Fri, 31 Jan 2025 02:18:34 GMT  
		Size: 165.3 MB (165316197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc5d132698379e2bcbfe17a7b915b761b9b51d9419db2ed8a4acc40ecda084`  
		Last Modified: Fri, 31 Jan 2025 02:18:33 GMT  
		Size: 81.0 MB (80993678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5701b5817d2b974a11ea32381b75affa99f82338a8f5c5b686ba45d0726040`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff9207feab209bd01fa1d105e1673e2a612464f13e80bb17d191d164a4af501`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:2d47302e63d057e67c732775232122eae8e338e9fb7f8bd08b716326e582bdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a211d6b348a5447e0263250c6a318b86eac2d3033bda26b23046cd9aa4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1960377ab2235eab2ffb5f2e999dd379244f78e5f2f61be5b942c79a9636e3e6`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 7.2 MB (7176767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f2d7c6b3dd86506ec156ba568306513c6a6c0759394bf3cac9ded812a76bfd`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53942cd1e71004f94071a83ac1691942c64827401acf425c46d16e66893e7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292495006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf13de6f15b34402f07870acc7c0a6a491e0b152f6f4e9adcc9fd90df00fd466`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c0578f01ece5f65df972fe1b35bda30fef0ae3cbb145784a12f99e0b7123`  
		Last Modified: Fri, 31 Jan 2025 05:28:55 GMT  
		Size: 163.3 MB (163341429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0c9fe35cf5e893d9dae2c2ca62c3b0c78d3d1e5183f18d0411bdfe042b956`  
		Last Modified: Fri, 31 Jan 2025 05:33:39 GMT  
		Size: 80.8 MB (80845642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e5231463f411254bd23c6ebc99dd220ff76b000315acb808e756dc2cd52c88`  
		Last Modified: Fri, 31 Jan 2025 05:33:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071c5986695f4084a1b6f4bbc9894be5e35c0a3f0c20c522d0a3639a0777b271`  
		Last Modified: Fri, 31 Jan 2025 05:33:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8d182e03b93d6c400e19b180e076bb80db1176d89707ac78a50886aacb1c99c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90881625c7e9bb70b6564e8b74fa787c93b5715468afecd2acba72c9fd4fdc4`

```dockerfile
```

-	Layers:
	-	`sha256:2086d292c9a7e8d2e0afcf868e24adfc3240db31d1c2d45df4c06cbb5a913428`  
		Last Modified: Fri, 31 Jan 2025 05:33:37 GMT  
		Size: 7.2 MB (7181933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4206f90b9592f8a056a00ab7478014051e6415eef70fbd7d69076475e7190aec`  
		Last Modified: Fri, 31 Jan 2025 05:33:36 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
