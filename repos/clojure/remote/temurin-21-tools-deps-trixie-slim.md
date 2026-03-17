## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c65b668c799909cd3fc944cc29873b288ab406b9ca58785a9f02fe6a0be0327c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf4ce3f7d73bffff2cdcab6f9c8cd44efccfd701f94a722b61c8e9128a12918a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259645817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2862cef418d126dfbe79e7bcc6c14d21494e7137cfba6db89d652788f3db8ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:40:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:40:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:40:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:40:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:17:19 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:17:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:17:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb505189910bc199c076ac3bb2347d9ecb604a5189192363af66d17a0db21ab1`  
		Last Modified: Tue, 17 Mar 2026 02:41:47 GMT  
		Size: 157.9 MB (157857118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0500ab27572549dfad063c046778e2299e2aae2cfebb4b00e97ce9c0aa77d182`  
		Last Modified: Tue, 17 Mar 2026 03:17:54 GMT  
		Size: 72.0 MB (72012157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d14913f7c3f24a92fde33795823f763e493b4b548b177736cbb0dcbd3521d7`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b31b5786f7a2401a0b83946d37007bf7afd1894bc9f68d0ab2b5ffb2ed3525`  
		Last Modified: Tue, 17 Mar 2026 03:17:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05ca0774cbc48f3e32321e8d7cb16167a7055c101b3ffe2908799699b19ef17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a990a03e460449439fdeb7b5020ab3c34471cf353223178188516deea287e3d`

```dockerfile
```

-	Layers:
	-	`sha256:f9ce247febc10dc81a0b6f53d46904df8f048c3ed15d9a285bdc795b44c51e50`  
		Last Modified: Tue, 17 Mar 2026 03:17:53 GMT  
		Size: 5.3 MB (5260990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:202eab32c70f55eac8c029e6749ca22daaa2cfc1a483692f7f08a93eeb9146b5`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8741b0e68718349b31957d5791bf07fbb3d02689ba9f53d030b0cf186e520862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941a8593966a9e787c80fa85b5d23b016be9bc25b6f9c2eba24d732a6255a36d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:45:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb513564ee1407eeee22eae7c45e107e887fee69943b91d27646fd7ddc81a8`  
		Last Modified: Tue, 17 Mar 2026 02:46:42 GMT  
		Size: 156.1 MB (156133025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45b4e8a5321b86536aff62080ae2e9870e0c735a619af3dbbb99d7c89d2f29`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 71.8 MB (71830403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa7d42d2d664146d54388ab8c6396f19c4c66d3f106a150d0c58b4a25d0107`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ad53575c7203178b5224d9612b04475851ec05731ff30b51040c7e2e1d09e`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0b188648e85442047c78f989ae724ebf4f010ba53e1fce8442a0a5ac762f0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8836f64b3d57c3a2e29b9fa0fdc9f03d490cc24780f9bf43506fa436fc7cec90`

```dockerfile
```

-	Layers:
	-	`sha256:effc1bf852227790cd779376e1e0854faf2f69220cffc42809e0b4ff0a967940`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183f445e0b91b6207acafd0146f8bd88cf0dfd121379451ef83f1b1c581159eb`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 15.1 KB (15129 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:51e98b00536a0e578cafdca75e5a611aad49aac7311e88008495def9265e713b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269007041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196689b3daae3e383dd083f00839301d47b3c4c74de1866abcf9f8016181b0a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:03:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:03:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:03:49 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:04:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7028262671fb5dadcebcc8bf5d066709ff6037f20f3a6dacd4f71d5d28a35f6`  
		Last Modified: Mon, 09 Mar 2026 21:05:55 GMT  
		Size: 158.0 MB (157977490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f2869619fc921515d3fdded2b0fdef33f2b9ba6e15ef780fa4055d41e1b4da`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 77.4 MB (77428288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f14f74ecff4abbd8712386c02b2696ddaf3a8426ae33dfa1d8cdefeb414840`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f44972a83cef7a1cdbbb34dfbb324fd4b1de5da68e40af7c82bb690f7be19`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f7001a3b75e77c360a7451f28d1554bfbd043b3de9a35525c3052064929dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3086f5da652f33a05ff0b32aae72f6587f8462787f83a2104fb8c5da050ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ff39406a782378ddba1eacca741e01553fb9d97813106e76ad0fc8320d7cb778`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 5.3 MB (5265287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42daa6b54a256337818e1c54c7d7fa9f42d5e4d666cc8904de441d6f54f1417e`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6fe2a4a9684742924a7540cffca96134e4e253f71b7158ebc1974668f06128fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256393854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d2760dc01c7e4cecd6f9b4c5cf23580c3cd0c6136a382b2d50bbaf89717d99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:23:47 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:47:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:47:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f2d4c20cb87ce38553ebd9ee153c1d2ba4124eefd89d1277f7fcbaccfbfa3`  
		Last Modified: Wed, 04 Mar 2026 11:31:31 GMT  
		Size: 157.2 MB (157216904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571881e3257cad982f734bbb80febd803b299e2063dff5c53c943ce6f6760413`  
		Last Modified: Tue, 10 Mar 2026 01:51:44 GMT  
		Size: 70.9 MB (70899486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c008bb54cab1c875fda1c06831458275ab51577dd26b9db4e55f5929bf1579d`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c18e158bb1824ee66ddd858c648436d473964bf5f0a72fca6273d52487fbfb`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45e019bc4c3b97e1d2d5f0137da517e9f8565bc985e5b08e08f92fc1aa9a6d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff93ce564c7bf3ef35950823e17da93a17616b6c90245c81d742b3a3c79eb81`

```dockerfile
```

-	Layers:
	-	`sha256:a89166c72a5fd45b5803572a49e76397c33e668ebf899cc1499d66ae65b0797f`  
		Last Modified: Tue, 10 Mar 2026 01:51:34 GMT  
		Size: 5.3 MB (5250380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04221e81007d18d6372b2d773659dc106204f8a778c3ff4233f71f794e40d1a4`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a214e162d422c98f86ac65ae5579c3b705e08af21729949a76e8ec5a14b3a17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4ec2f1a7661f4d0ee9591011abc068a82c31f4adad98cd2e60f4cafa8f5c12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:43 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1739455c8adaa1831c28f6e8345aa92a5327b6efcacea5168e2647078f0e63`  
		Last Modified: Mon, 09 Mar 2026 20:37:32 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b0847a2070dd3a416be85d53c4de86228b82a1cdd7c43642a3daf5e9e2c0dd`  
		Last Modified: Mon, 09 Mar 2026 20:37:30 GMT  
		Size: 73.0 MB (72983703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2476888f386cb12ad521ba25efd3bcef44a9a2ae826e12082715d64b3da4be`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868dbbc915c30e4b0e0e9469d545270c3f61ecad90436101cc4507dae8cbd135`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d14bb29593b312550beab0af9d4fa696ce907223c5b6db3589649c05122d6b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b1303955a5d8848c395637bd24fb55c67e9e933bf5cdf798805e9085869b5`

```dockerfile
```

-	Layers:
	-	`sha256:1c287f4a98407ae083ed6cee2d7ebc2317fd4d2c2b977ce65bd81cd335b69495`  
		Last Modified: Mon, 09 Mar 2026 20:37:27 GMT  
		Size: 5.3 MB (5256840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c90d86da52254d720abb921a661f635bc0e381a5f9d27cd62d09ebdedbee54c`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
