## `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm`

```console
$ docker pull clojure@sha256:9178a1f38733efbcb93bf748f11cb6d5881c43a20c90b54eafcb8d5c0407f569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d823d7accabf5f61c66c93c91b7a27c27a68dde6e5096dfa9683110363b8c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275073345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43f8877aa90d5a6eaae1130a8d531f29e147e884af8d30e75605a84b1db575`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafd06a26b4980236142ab269ae3bc9611d8ae43fc8147613242afeb6b4f87`  
		Last Modified: Fri, 31 Jan 2025 02:17:43 GMT  
		Size: 145.6 MB (145598781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0232d7780eba4151b58ccf285271e0bde2fa0f7f53eccf73232c84f420e347`  
		Last Modified: Fri, 31 Jan 2025 02:17:41 GMT  
		Size: 81.0 MB (80993956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107655a717b3dfd8cfd4b87ff5e6a95b5f0344ec53260b374c34295581305ae7`  
		Last Modified: Fri, 31 Jan 2025 02:17:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7aab531d270d2435cbabc561c3c39efbe97b423bad454df03d4c81886855f606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eac31f3c7c76cc2bf649a942bd1f7c2d74f63e66b11ed492e522b3ec64775d`

```dockerfile
```

-	Layers:
	-	`sha256:baa60a5a5ff5cd405a550c961ec28aa63889d096a3c96b25a3b6200744e64072`  
		Last Modified: Fri, 31 Jan 2025 02:17:39 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b067cbc37c539507f76a0b64de908963f666238e0436361b667c66f62b3fd8f`  
		Last Modified: Fri, 31 Jan 2025 02:17:39 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a5313cf1a3e2106607554c55a49accaad7e1d516aeb174a0347c37ed1ab38d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271538649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca83d94579d4dd4eed5c6df9ed9289abec7d8066733fecdbf3799790d66ed3`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da991aeb9179874ea9db6574a6a0f7e557d853cc6a751ebb20b9e551b36a8c76`  
		Last Modified: Fri, 31 Jan 2025 05:01:08 GMT  
		Size: 142.4 MB (142385531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5538dbfb2293faa525d93117aea9350c641ac4af5185eb47afb3947ae6a0404`  
		Last Modified: Fri, 31 Jan 2025 05:05:45 GMT  
		Size: 80.8 MB (80845576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623567aaaec3dc3aa7c838cf3eb6a3b41db6d3de2e12336d2cd9c5fea1f5dfe`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2887c56a4253b13a296c01b9f9ce19e5975d502bb6c1e1c7d71f47efdb400ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261c48bce94cbcd29c5969b29db1ce842e530548fbd66133462f4105651397c2`

```dockerfile
```

-	Layers:
	-	`sha256:d585de443130b667d6595d9abe0a92406c43d040276144d894ff3d27074b2cb8`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5ce6d71d60daad4bf72f8419ef996ee36902b6f40e2ee6e4041f6dbcf13768`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
