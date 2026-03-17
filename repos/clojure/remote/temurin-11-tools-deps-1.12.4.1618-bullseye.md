## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:bfbba1b700c17fd24fe91c2bf51a7ca6419c362708376af07b839848b961380b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9681fcf7f2295558fc2b85c60a6a95253d58e8f50a976dab9b2333ddedf94627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269157903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236f2e84a3f57cf1b224437dd7437c776c6b1e6437f44f76c7db7cdf9f8adee3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:25 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d2a303e31e3813258179ece943086b09125b0d2cf6e9c62be8a992de1dc92c`  
		Last Modified: Tue, 17 Mar 2026 02:58:01 GMT  
		Size: 145.8 MB (145806960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88099db2086ce4c402f5829ce4a89c183e6455b0479aa8615f31c7e7b9db21`  
		Last Modified: Tue, 17 Mar 2026 02:57:59 GMT  
		Size: 69.6 MB (69587817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd3cd659eaa056a45f977798c1ba02fc36df7dbe2af3542e72c003aefac439b`  
		Last Modified: Tue, 17 Mar 2026 02:57:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c8ab993f09f9b68d276a491aa20d6197772547a432d9be2728a8dbdc01ab1ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d80cb72609bd4575c8801bbab176ae4f27143b5bb38215fef3c9cb2a9e3106f`

```dockerfile
```

-	Layers:
	-	`sha256:d9ead3fe09e060d7aa042e529dffabd98ea98dcf70b6a278b4702410aa734122`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7055448cfad2e238019f5852f15478cba435be61d02f9492049cc88230c4f52`  
		Last Modified: Tue, 17 Mar 2026 02:57:56 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dad284438ea84e96d7f83b0f30f7b4cf5990b6e41598a24f061dfad77918a042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264476033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c661e7c54d10aa7f4e87de32d9c847a441d89b5101e6a0ebd11af0d49740b3e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:01:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:57 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb1b709adcbc0130c2b130e73cffb3e4452dd170ea9f0e2a2e6179a08aa4713`  
		Last Modified: Tue, 17 Mar 2026 03:02:40 GMT  
		Size: 142.5 MB (142500050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df1590c4014e357c50d03c98c0f0c2b838b8a6f8cd131dfbb602b53ed51394`  
		Last Modified: Tue, 17 Mar 2026 03:02:39 GMT  
		Size: 69.7 MB (69728084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec6b42e27256874be8994294c0c1e4cf9b9c09903897058ed17438f98944d04`  
		Last Modified: Tue, 17 Mar 2026 03:02:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e5ee42da1a98967f4f2e0f4e0bc14595bb9d6cb6d8386aacd3ff2bfd8d12d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b82c5f0c3f4b6b1280603e141fb6ae366a84e747cef7b6a5e01348a2c1fa4b`

```dockerfile
```

-	Layers:
	-	`sha256:50e2b10ad55c373611baf9bc51933096c5f135b8e47af67fc1522d5f03871838`  
		Last Modified: Tue, 17 Mar 2026 03:02:36 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99c6823d98013219bbecfc8e3bf84516fb27de6781dd468a359c75f6eb47415`  
		Last Modified: Tue, 17 Mar 2026 03:02:35 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json
