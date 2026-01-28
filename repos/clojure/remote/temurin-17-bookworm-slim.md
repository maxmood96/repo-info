## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:d0f6150d619306c12b10010b972b67e739f5882e73d9c535719101d14a5f37ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8c5ebbe94e73a91246ab3810e2db9d2e71c328c889705e4e51d3ac624372808d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242755303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1686428a29fbe87d291ae72de735cf0584508a228950e8506c5b2116d8d9ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:04:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4289994a77e828f49eb75ad121be08260b3fb931587461ff1ff32315abfd2b5c`  
		Last Modified: Wed, 28 Jan 2026 18:05:16 GMT  
		Size: 144.8 MB (144847973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ee7dbd999e99d1b3348b54ab453ce5cca1ff5f9e2a8baaab6e4b2eed1c604`  
		Last Modified: Wed, 28 Jan 2026 18:05:15 GMT  
		Size: 69.7 MB (69677715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b27645dd7aef02285188e7d2ca526fbb8f1f31718f5298f6cf8ab9c79336b`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031282587a5b9a2825e14fc6dcd454d729fcc3ba53e1412bdab2fde829db5e6b`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21e11e59259a20704e1930f79b2a00317616d8ff4b87e3077adfb57cc27c1fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2a2238e63e1c942d27f2e18b4c93fcc9de21047a143cd7b7787aeb646b1fd1`

```dockerfile
```

-	Layers:
	-	`sha256:9acf16b48a37f6e2ca80d480b0d93eb76ed454384653b2196f4c5df790d3a765`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 5.1 MB (5113402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aac6633508003f9fb121c288ce50ad4951ab368387c1a3d23e24bed0295f121`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfdf22a3fe99bfcd70eaa7dd3d75bd2b147dd4782404c841f982b96aa3c92f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241461606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c314a96384e4dec56324591ebf9537dfe694bc8714b9b267bd11fa871938afe8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:04:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:06 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:06 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e3de3dc4c2f5daaf98842e8f6fd9139db07865c9e4c9e1c4d90e55dcc83140`  
		Last Modified: Wed, 28 Jan 2026 18:04:49 GMT  
		Size: 143.7 MB (143679932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b0c044a2f74de6504a69859a2561953fbfe7530840be2bbe256b6b78b30cb`  
		Last Modified: Wed, 28 Jan 2026 18:04:48 GMT  
		Size: 69.7 MB (69672745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77031cd3890a5e470544224def29fe0308b753c0a66019c08a2528c195e9d50`  
		Last Modified: Wed, 28 Jan 2026 18:04:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546b8abcdd459ab78d3fe1b3ffe9dfa7e4813e39d3557ac24a64f43af8685815`  
		Last Modified: Wed, 28 Jan 2026 18:04:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3c1f4216a1d82c39126d317ea4a30e3e54b482cf6264a2f1ba65ff23f15f9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3766b839b3d31f8f7b640df6d488a3a048b97fce131facc99cbd9dfaccfbd577`

```dockerfile
```

-	Layers:
	-	`sha256:5e5e31acdaf2726894e59e86847b06cc66be7d2554150775bcba5a9fac114973`  
		Last Modified: Wed, 28 Jan 2026 18:04:45 GMT  
		Size: 5.1 MB (5119163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b1b95a64d4b49b2c2b57ee09637ce0b99b786039461b842a6d80bdc54b6737`  
		Last Modified: Wed, 28 Jan 2026 18:04:44 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d79810c9dd08716e2d466088d3a6c95f2f14be399e21ff5bf8c20f020220d366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a17618f318b991875309a1448d6cf2a183fc99b8d9fe3188de3250253c541e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:23:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:23:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:23:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:23:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:23:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:23:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:23:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:23:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:23:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2235c724473658ab8b44f8727ae7cc58c2e9f4d98756ff0ccd8703501e42f498`  
		Last Modified: Wed, 28 Jan 2026 18:24:33 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a8e4bcf1f532479fe5324cf0f32878ca76c90a1b3dcf2c3078fbc8e1ff7a2`  
		Last Modified: Wed, 28 Jan 2026 18:24:29 GMT  
		Size: 75.5 MB (75513981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98697a8313e90de9363e8094c714ca833538c42e0f87c751e7a7b52b91e10db5`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ed640ff49ecfab009036a763a4360443dfaaaba06f8101fe437a05d025e438`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8728042d3c8ee56020a604b741c59d33e4088fb962e877803abdb1e2ab23812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577eae15a27ba8c1423a650f05452e25002d3fdcf9a552a8e9577da0d6b2c0dd`

```dockerfile
```

-	Layers:
	-	`sha256:e0dd961e7f80e8e60c7ba44e3f456cf7c869f59af799373b91123f5c7b30488d`  
		Last Modified: Wed, 28 Jan 2026 18:24:26 GMT  
		Size: 5.1 MB (5118560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b37222b05abb620dc3159ff832cdc3ef40eb04defee0ec97e58ee7bba586a0a`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:942091f2c00d9f289c950a15fe07109520f4c73b8d539c9ba2b49dbe3556ac0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88b1791355f19c38f12eff785c9741537da2b893eb872a71182062eb2f314ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:16:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:16:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:16:04 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:03:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aab18a387fc18c5b933990f24aae256bef846e7ea7b8f21dfcc273a36931821`  
		Last Modified: Thu, 15 Jan 2026 23:16:48 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d4bca2a4c65e64214d5f96fb2c9c8732b5cb2f93db8762ced098fc9f795a11`  
		Last Modified: Wed, 28 Jan 2026 18:04:11 GMT  
		Size: 68.5 MB (68490138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669de6314d83a2974ff3f3aaad766b5b788a820778d05f5281bebd0c33725d57`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19aba888a63ffc62f99ebce72c6a40b060abd3862c9230065f1d82d16547496`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e61af33396cd06b57797f1b8d48811cd2856f819564ec731b3bc2976e2079903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19af2f1e90abc3dd5fb39a0cc3774596dc0db42c82216111b09569546ba39bed`

```dockerfile
```

-	Layers:
	-	`sha256:61bc7dfbdd269a2609f9ca6c05ea5d948270e09ac50feabb54d8ae785e5a7f21`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 5.1 MB (5104723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a82c560ee2c8ff5b40e877074a94a2d9dc0727deb1e5f007ba126c554adff1`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
