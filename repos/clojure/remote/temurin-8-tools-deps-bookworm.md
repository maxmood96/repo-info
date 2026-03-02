## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:649fb96b36c33090ade0dd2f80aed2a9a91433dda0749e0b000bb43f48ebc996
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:be384805927823fc61e52812ae2e24a3870be9ded37327f8b471b5a35f3097f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184820841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f296ecda693545e84c38baf24221a0bf1e00e7136eed3f21a092e21b4d30af6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:00 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:00 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03834438f796741be834c5c62920b14831c9844b14747fecdacb8984766ea94`  
		Last Modified: Mon, 02 Mar 2026 19:45:36 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd718700d4aa588cbad6b9d3799ac8f682a4acdd464addf8c7eacd51aad98a3`  
		Last Modified: Mon, 02 Mar 2026 19:45:37 GMT  
		Size: 81.2 MB (81161356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7416bd5872a44f3150f8a52657417770bdaa690b9b9d03939903daae77f1f3`  
		Last Modified: Mon, 02 Mar 2026 19:45:34 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2e434be9a9acaced6c5e5b7f566274db8a25fd024543cca064b9935e2f64fc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409b43b0053d4782a5278acaffed788fa5d70e7aecda6d1d582c349ecb2ee97b`

```dockerfile
```

-	Layers:
	-	`sha256:dac849c601f61f76659d30876a1283f173b97dfcdc0d42c86d71269b1b7fe96f`  
		Last Modified: Mon, 02 Mar 2026 19:45:34 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e54d02d63629457d875a8515cf671b10aeafae19b70f59dc258657dec8c070e`  
		Last Modified: Mon, 02 Mar 2026 19:45:34 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63eef026ff0b9705984dc8091c7ff4500eb05dac151f72febef99a843f8f7d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183780343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff410ccf61812c032c9fac9b9152cc8a18257c4f8aa4733c710828ec69e0bcb0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:25 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:25 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988bdc2961e4aa4c1b4cfe096fc30d78464821a24124da3ef79e23da6b21e8d0`  
		Last Modified: Mon, 02 Mar 2026 19:45:59 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ded6a72ac07ee3f1ba8596726c722ac83a5b64bcc5c774d06dc8b27c159e0e6`  
		Last Modified: Mon, 02 Mar 2026 19:46:00 GMT  
		Size: 81.2 MB (81154869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec5f47121f472a4b5c15aaf4503a3a1a23546b222d16a160e681c9091cbb2a`  
		Last Modified: Mon, 02 Mar 2026 19:45:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d8eb4729416537adbc937a19d0a3a00e2fce6e5296ac23f240de29536f344d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752751599d7c45fe7f16ee22e4f35bf1a5046cb31a2d180f96f4521b91380e9a`

```dockerfile
```

-	Layers:
	-	`sha256:e6f1cb332075b8357765a438086a8154ee6f71b7f8cecbc5af8fbf1a8b4f6bf0`  
		Last Modified: Mon, 02 Mar 2026 19:45:57 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afeafb09f311197c58994fe4abe67b326eb825c72e52cfdd6f91d36382d9076`  
		Last Modified: Mon, 02 Mar 2026 19:45:57 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0cda21aa502c8ebe82de49271b4372cdf533e92bf717e936cbb22898438d13b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191991147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3875f4a79b28a5be145cfec3b359a9214351dd6fc170731e48075617a2d386`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:33 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:43:34 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:44:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:44:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc4949417ef5f9fb8be4426d9b9089efcede886f97f903f40d7f166cc416442`  
		Last Modified: Mon, 02 Mar 2026 19:45:33 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbc040eb2410c9fa5f23b6a62db43e4c12b3df53312c537c7fe9cc92a0ff827`  
		Last Modified: Mon, 02 Mar 2026 19:45:33 GMT  
		Size: 87.0 MB (87003312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617e2e0f9f5a4158b6037702641d75e32b30f74537392d16cdf2f08754201d2`  
		Last Modified: Mon, 02 Mar 2026 19:45:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50f26d8b6296c919bc77b1a7b91188ef5902a50b24ef27700b0af8959ad5c3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0d9423e0e4a4b2ec1ed3d7124a3b95f1d6ae7de374e90cd1d7c878330b86ff`

```dockerfile
```

-	Layers:
	-	`sha256:282809c4e0242452f943f4aaaf63ad2eaf0cdea951bdf075260517d5c4404251`  
		Last Modified: Mon, 02 Mar 2026 19:45:31 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc6cefa24123b605697652426f249446fb313effda685506a9b96b6639b5bae`  
		Last Modified: Mon, 02 Mar 2026 19:45:30 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
