## `clojure:temurin-8-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:092090bd92811b278a37549051135b8422a9fa47479066f5632e070fc4bc855e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ed3b4f066d932e42cdab610ac0f01ebf02aa400a63e6795ac6c7128d064f0391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190031320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6461a72dd5f4c0b7fb02d4a5a88169cb6ec636ae43d2722891724c1c816c031d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:53 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5076f4b3f39a3114ab11070b4b289dfa2852d5aa2f1936c296402b3f6713628`  
		Last Modified: Mon, 09 Mar 2026 20:34:31 GMT  
		Size: 55.2 MB (55170084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7914db0d1a2fa585abed13acec3ae5a87082715edb97a89c737ad4cc6a0202`  
		Last Modified: Mon, 09 Mar 2026 20:34:32 GMT  
		Size: 85.6 MB (85567465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a29ab3c1605ef1fa254734dd021dbb77a4b15953d27fb98dbed00b2afb6f0e`  
		Last Modified: Mon, 09 Mar 2026 20:34:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a12ebfc539e93d18ab69662fc88dc4c471c53a8b2102ab881415e02426a91ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4a6350184bfe9e46809c349d5172e020ee2472cc9a9078d98adfc30b4d6f18`

```dockerfile
```

-	Layers:
	-	`sha256:b540d354922c41ebdce6715accefc368139bd7148db6d30986a1f5826a0c0c19`  
		Last Modified: Mon, 09 Mar 2026 20:34:30 GMT  
		Size: 7.6 MB (7591580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67edde9fe34ff9bcd538f5e1b1531ce675a57e5b52b6d7361f42d6e43f32906e`  
		Last Modified: Mon, 09 Mar 2026 20:34:29 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:744a17b63ede3ae401cd5393e1274508a50cc4db9b944ed250d8f6282e81de5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189287297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb20c991d213b81e204c8b21ccc091e20776d88168e98311de3389f0e3b1f060`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ee855ba14f0a5b803c184a931abfd2396a0e6f79f86150d093da6bbdb1b24`  
		Last Modified: Mon, 09 Mar 2026 20:34:27 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e52d4e114bae479b5bfb14e1d95499f7b781bbd47b19704ca3e38a5ea68314c`  
		Last Modified: Mon, 09 Mar 2026 20:34:27 GMT  
		Size: 85.4 MB (85382867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d80c1e1aa9f66a22acde118a9b4f20ae71b6ee4928be6b803bd44b34f62039`  
		Last Modified: Mon, 09 Mar 2026 20:34:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f5075f5fbc780e161a095451a2fef9fbebea7a728289b3724a98f5a2e5191856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f4b4024db72c85d6c2e24611085b84ff50c8494630bece94ff8ef46611f1e4`

```dockerfile
```

-	Layers:
	-	`sha256:0ca2ff15a927c3b62fd7d438f5e93f8f8642202065d24fa379c9ebca76c84174`  
		Last Modified: Mon, 09 Mar 2026 20:34:25 GMT  
		Size: 7.6 MB (7599310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43205c29c4959dcc1e9335cf8eadc760dac7c88ca3f8909bd6fa255b2ccb05ed`  
		Last Modified: Mon, 09 Mar 2026 20:34:24 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ee255fd6253c71637039b85f1fb6e17b1672ade342c3fae7b053750df5fdfda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196739968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff40d5a04f130f6575ae16f2802af4841520b3b030e9d8b0e9f28945221961e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:43:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:43:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:43:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:43:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:43:50 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:44:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:44:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:44:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f433cd6a7592bc48b33b544e10a803a205a566330f6a483acd14d8b1279a0`  
		Last Modified: Mon, 09 Mar 2026 20:45:16 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3309b696921326cbaa9badf9d61f8a1348976a407d6a70c8add36ccbfcaebd`  
		Last Modified: Mon, 09 Mar 2026 20:45:17 GMT  
		Size: 91.0 MB (90976671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a1f9e43b8c502b18d7896b52282ea15e0d6c063e84cec2f05faa0453a21fe`  
		Last Modified: Mon, 09 Mar 2026 20:45:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3d0bbfc6350815ac6425f715ec7c5e44f87b18c5b0b1e02b423208dbdff220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff9ba86e88ff826aa6a7158ddac32f0a52924dbbf5cd6e6949063e4beab6ef6`

```dockerfile
```

-	Layers:
	-	`sha256:6f786c2068fe00da6a2c04941d71a58d7ae6748ec2301245f99cec89a874307d`  
		Last Modified: Mon, 09 Mar 2026 20:45:14 GMT  
		Size: 7.6 MB (7596596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942895eead4b677a45ce173ffae3a8b927b936267e10e9583db25d40f8e9dc16`  
		Last Modified: Mon, 09 Mar 2026 20:45:13 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
