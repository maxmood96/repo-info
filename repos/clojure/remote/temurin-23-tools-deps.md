## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:5ae6b2dd97682ebc98ab61d69c64b4da2cba2e3181b7c675ce439e8adf5c66bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:6c89d6f4d135b1093a58e33eb92f280cf55cad597cf00d66f7e90b6b861cd990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294790807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cbee3d4f026388edc0e3f5f0b223ba8af691f4095c6527e6251cdcd98bf4ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5677422e15f022261e12225e1b7497c6f0c894f6a02923084d2b10421534842`  
		Last Modified: Tue, 04 Feb 2025 05:21:42 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b67f43b231dfead60ac1d7cfe8a4b483f3ae767447e97c1fe8047b9a93324c`  
		Last Modified: Tue, 04 Feb 2025 05:21:42 GMT  
		Size: 81.0 MB (80993899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d417198751c159f59371031d98c01fd82088982a21dbdaaa528ab3d2fe64c35`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d36bcb7435921d7a0f49bc6862bf092722a664e61eeaa87566438012109f72`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:5ea9d4fbcecd5b55ba13c8aff639a4f02a8051c354efb4474910a59cd3dcd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838fe5fed4405de83bffa944eaa4bf9f08c916231f5f7eda9bdd1fbc3ad9aa8`

```dockerfile
```

-	Layers:
	-	`sha256:1a1315dea731b4c3a7632575f7849ac26a9909e15c8c3e57b8a62605c87fd907`  
		Last Modified: Tue, 04 Feb 2025 05:21:40 GMT  
		Size: 7.2 MB (7176767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad50c398349e79fb01b44dc2d42dc142c7635599ff65573e09efe84f0394ce9`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
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
