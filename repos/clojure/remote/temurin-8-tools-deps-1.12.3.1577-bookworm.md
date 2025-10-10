## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:d974e5b2c61759958b4a9f84af4122aadd6f44509a9ebf48e48fc98af3d4e037
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a7450231d933e4349f1b4d909ea58b14cffb47460a154765924c8f39a254dcd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184359563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4149a7a0d3320964d528f3cce1677a3120714e35d03d241ee939c11753ad712a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc9823f10cc46adb660b05f9cbafae27bdf2bed2ff1f385c6002de843640d03`  
		Last Modified: Thu, 09 Oct 2025 22:26:20 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2319cda1ffaafd34ba14f23311433345ea30e6959c220930af2a4bab0af46772`  
		Last Modified: Thu, 09 Oct 2025 22:26:21 GMT  
		Size: 81.1 MB (81147011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5faf92f02576d810b85a746abdcd1e5a8f31403badd8e5bf4a8ad185f866de`  
		Last Modified: Thu, 09 Oct 2025 22:26:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9cb7ed09f74d24da0198b2d172e57fa1cc7ac82af874fe32ed8baa9f663322a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa1ea0a00e458cde597d84d2ec2a4fc81c765dfc1733bce947305e8c29336a1`

```dockerfile
```

-	Layers:
	-	`sha256:87d21bc1b8e8b69960b365058a3c9ff4b19cd2ee660733a0c58eae293e2fe17e`  
		Last Modified: Fri, 10 Oct 2025 06:49:57 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5c73c84054e5f98d94f1996989437cf969e9b4996260c31d2fe8021e0ec024`  
		Last Modified: Fri, 10 Oct 2025 06:49:59 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c845646a552bbe29f99c7bb5ee29c0f520fa9ff1b1b8952449eb67e80e40166a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183225250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433cd53f41fcb210a25622fd06742c08d30af53b7365cf1be6f5aff7baf770bf`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6b9a29e1e7a9ba750432a6a921e104b43e2e51eb5e89328cd0f3d55a617221`  
		Last Modified: Thu, 09 Oct 2025 22:26:43 GMT  
		Size: 53.8 MB (53835637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3111829195a53332634c8af8af804651925602f5f75dcbe5b3becec9acff8e`  
		Last Modified: Thu, 09 Oct 2025 22:26:47 GMT  
		Size: 81.0 MB (81030053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2910e7ab1bc63ce078fe9c1a87cbdc099bba1bcd70314d0b4926d8769cf8193a`  
		Last Modified: Thu, 09 Oct 2025 22:26:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f9253a70fc8f10ab3816136b056b273be663aeefc34263684b71ccc516ad5613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d19bc91c2c3c584bc9c8736e63106deae2abe2193bb848113670e4806572ed4`

```dockerfile
```

-	Layers:
	-	`sha256:f2a9a884de8a320a4600137ac8f4412972cc9598297d8227787ead4d20e02480`  
		Last Modified: Fri, 10 Oct 2025 06:50:05 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17947595eac442d780b939c1cb8480c0bf348b649d9a63a586b6af7282146bf5`  
		Last Modified: Fri, 10 Oct 2025 06:50:06 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7e8c4b593c9e1ad5cc15ca9a83d21bbfc63c2efe33e5a10dfb203f893a03c3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191478684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b659d3490ceee2c5ade423e8fd63a8cad871dea9d50660ff6578098d31b918`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ddd0af0f7ebbdbb14517b608732ced7b77f026bd12e988950f03c5eea95a4`  
		Last Modified: Fri, 10 Oct 2025 04:42:10 GMT  
		Size: 52.2 MB (52165400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b61e1614548b02ae50c714b219cda14d31bc55cc5fdb07679882917faf0d65`  
		Last Modified: Fri, 10 Oct 2025 04:49:13 GMT  
		Size: 87.0 MB (86985873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6121c513a27b7934f556e6a28ea5aa57b12c61b7664d75a20ef8c80097732`  
		Last Modified: Fri, 10 Oct 2025 04:49:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9e438e9086ef28235ec33eb32a6b6b37fadd5d0cd9f80a721bf56d8e360bbc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed68d1cc62b08068989874a45be5d3b51724e9de325f2a4a03bcbce204fa8d`

```dockerfile
```

-	Layers:
	-	`sha256:d2ec13124939e3da7f545922a79e6ecaa341fa56ed434d3ef3b4cc8dc3494f83`  
		Last Modified: Fri, 10 Oct 2025 06:50:11 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b7c12a15c9a658baebbc9ffed8f6b48be747b34f6cb750e22792804c2f5cf4`  
		Last Modified: Fri, 10 Oct 2025 06:50:12 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
