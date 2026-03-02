## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f393612944fc9554a39c9ddc1ec2a8395e58bcc56e478ef5b0ba4bc581dcf3e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:985197facb229ee0b49714999c91ad9a7294bf0370d5663e06e921ae253bdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153098354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c09c95c508ff5e4ac6dbed2b51da1b529bdeefc8c8243f6426ce24a9ac22ee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:05 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:05 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becf1b52dce0e894260935e3e14125233ed3346ec464166bc8fe131369ca8cd`  
		Last Modified: Mon, 02 Mar 2026 19:45:37 GMT  
		Size: 55.2 MB (55170084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b751085c08dc930f5211f4f1166ef2c6377732b94545a3b01a420f3b4c005983`  
		Last Modified: Mon, 02 Mar 2026 19:45:38 GMT  
		Size: 69.7 MB (69691347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5cc47d0b7e5df953ec85799d82e4b456947b22e451acf0243cc3ce966bb762`  
		Last Modified: Mon, 02 Mar 2026 19:45:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d223cf4d9d0c0f2c6e6467c8bac8f65451227a0f99760a7f50d074220798c59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd267b026a503f8299c729adbe7e94e60919fe71dd484634c624f64a2a93aaa0`

```dockerfile
```

-	Layers:
	-	`sha256:fd478bdbe79734890808cf8be3559d7c8f5d40ac8d04e24b2e7d28abb9fb7557`  
		Last Modified: Mon, 02 Mar 2026 19:45:35 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ad773ec783c89889d22be943f95a3c0e6036fccb3493e61f78ec86d0369e7d`  
		Last Modified: Mon, 02 Mar 2026 19:45:35 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c00fa1f9b3aa69e074a7e54eff2a03747b1c7492854e32e960539e088861ae9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152056437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02528608ba8a6b0a304a6b61afff50d9a2725da1a0bf3f3f817b6f788f55fff9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:11 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:11 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b52dcca48830c76d9729e1943a1e5bd2670b1737e445553e6d8c6428574f61`  
		Last Modified: Mon, 02 Mar 2026 19:45:44 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef31430c2e40a9e6f9ede4d51eaef98a40c4083920ecb0039a125fcb15a31bc7`  
		Last Modified: Mon, 02 Mar 2026 19:45:44 GMT  
		Size: 69.7 MB (69688090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b4889a9a650b9aa26f4a39acd5a401b9a6862ae103c9644df1e1c144fb7189`  
		Last Modified: Mon, 02 Mar 2026 19:45:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20923c75f9264eddbcc949f33377e657aa99c42c5893b6359d9d04c457fc9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7a68ed84f8da432218cdc6c60d01be81537bab6399cceebe51ec7f6bef687c`

```dockerfile
```

-	Layers:
	-	`sha256:66d9f62dcabd8166812f7610d5cf5f133f6173191b81745db96f03ce6b38f47b`  
		Last Modified: Mon, 02 Mar 2026 19:45:41 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015ce311170cd8bebb3160e2f66b22cd39ec5defa2cd7e3205001901540932b1`  
		Last Modified: Mon, 02 Mar 2026 19:45:41 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4d9c8d49324337529ea5f84a3088b4f33caddd5b750be84bf7577d0dac5f1101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160257213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc2bc0e70674fcbe10be2f5a01d8b2743225a9409edc39460bc9d2b5005664d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:50 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:50 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba352d5eecfdde7613d51ea45592007aa92452673339a110dd3f86f06b2ceac6`  
		Last Modified: Mon, 02 Mar 2026 19:47:10 GMT  
		Size: 52.7 MB (52650417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e29a5c24f146eb699732ce09c30362bb12c956d0ef7c1c8d9ed6ec795ffcd7`  
		Last Modified: Mon, 02 Mar 2026 19:47:10 GMT  
		Size: 75.5 MB (75527815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf964721ff672e128bf2b2db2744d9cfc359bd2e7d4006affee9e1f8e8fba83`  
		Last Modified: Mon, 02 Mar 2026 19:47:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0daf2579727b6b60522391896c8f64421a526732654988fd1d3cb3733e9d2aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc1bd1a890997745382218d586a9018a41fcdd3e90324c034f2c1f20e04c6fc`

```dockerfile
```

-	Layers:
	-	`sha256:a9860e36216ed96ccc3c3924ae52914707d5a426d839fae912b87da8239ccbe6`  
		Last Modified: Mon, 02 Mar 2026 19:47:07 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fda82c2772d3da9af4eebeb37d985caf0b7f1d6f6ff71a9443a843fd1d1728`  
		Last Modified: Mon, 02 Mar 2026 19:47:07 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
