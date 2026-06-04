## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:8c3c8458d02d9d1cdf9c94152d8620709c470b0b16bd3cd4844d5c97a6e5e5f7
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:93572baa5f0e7a005594915d72a0123b19588fa1d4a73dff9fd3deaaee6ba221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187450882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89148317b485f04e12b35a5aea78c3e47cd9cf38f59a0387f0605e3afec54a8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:18 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ffe0e6a3471845070d76cd18da1665068b8ff87ad9142db18903c5e86f06f`  
		Last Modified: Thu, 04 Jun 2026 17:47:55 GMT  
		Size: 92.6 MB (92574616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d76cbb5e4275cb7d983e847ea27884de2e1105da019b342ea6f5187277f2e12`  
		Last Modified: Thu, 04 Jun 2026 17:47:55 GMT  
		Size: 66.6 MB (66641681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed64783a85a70761692b5447f410b0ab31fdfc7921f3bfb45e37cc932d44cf`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d5bc7becf694e726ab4a3c9a2f45c67cb9853880e94045d381270b6039d5b3`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c3e0dce7646979d9442f75e136e05a0d337f4b18e53f27ed5fcf89b2467007f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5098750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ff8c7bf0a5a466c09498f6c2073681a45d90c83ea4761e479eb81c2f2057`

```dockerfile
```

-	Layers:
	-	`sha256:77055154e54d61d34ceb43f46a2af185842d0b0cf91c63c7c87d43231f1e52b2`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 5.1 MB (5082071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e6ee08137943e25c7f1fe5f0afff204a487dbde28c4381055db79bf1c01cde`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa13d4bb2897a86c7becef67b52a35d5ad0d74b9535783b5c48113c65261a9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186301395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf128fa199535e8577982ad7c00c135e818388e0d7754f5c7dfcbc7540219bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:09 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:09 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d403bba66811ecadba948ec51af5e2406058b63e944bda7dad839258c5c2ff3`  
		Last Modified: Thu, 04 Jun 2026 17:47:44 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360d3fa1942742328d06f4171e140f5aa295e2b9a7f62ca23c5ae0ce3ef5997d`  
		Last Modified: Thu, 04 Jun 2026 17:47:44 GMT  
		Size: 66.6 MB (66643052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeee051f76d4716b55936da52c0744d4b8ff66875ea4697a9b3db0f66719ec2e`  
		Last Modified: Thu, 04 Jun 2026 17:47:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ba8818c4946da59b4d9f6a256db74b979675afe21d8b6fd78daaaebccbc1c`  
		Last Modified: Thu, 04 Jun 2026 17:47:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92df3cdc7cd010eb363d845a367e1f55566165650f8daae4f9fe9a11f621530a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6f39da588d16641e0e5c59e9e8b4c9e93942b228c0afebb009c46bf61c81b0`

```dockerfile
```

-	Layers:
	-	`sha256:87b660df5251ccca7116754e2b2c98c305d35150c643bdc1951145dbfa37b2ad`  
		Last Modified: Thu, 04 Jun 2026 17:47:41 GMT  
		Size: 5.1 MB (5087853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1200a286ca715a176ce0a5eb1f0f0510ee5535655212e3a9854a2bb969974245`  
		Last Modified: Thu, 04 Jun 2026 17:47:41 GMT  
		Size: 16.8 KB (16818 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e9e9caeab959c9cd4b2848d4145486aa5f7c3779f312c8418a0497c3a512d357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196466680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39650bd4be8540987b53df01ea47d564c840a81f75d1c77e6c42ef886d771bc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 18:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:04:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:04:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:04:47 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:05:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:05:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:05:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:05:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:05:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ef6276fa52e193ef055bf9f36e8433b5fa6fe3a3c3cd0887000093a669d38c`  
		Last Modified: Thu, 04 Jun 2026 18:06:18 GMT  
		Size: 91.9 MB (91914019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e2cec2569f37ce52fe3276caade59ef9ac92e7d66e1e9303e7c4684d64b070`  
		Last Modified: Thu, 04 Jun 2026 18:06:17 GMT  
		Size: 72.5 MB (72475875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93f3d036388a1207e37cf14e07a8ce28028e5c9e7784c1923462dd9ffc893a`  
		Last Modified: Thu, 04 Jun 2026 18:06:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef02620fb76b0993f270f3d35ca21d654bd1d889c71735b258b3e5220e3694`  
		Last Modified: Thu, 04 Jun 2026 18:06:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d711fa4c859ceca885b5f9290c9378157f94bba9cc25c290a6e655bfbdcab505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea8c8e5a24f87703bdd3e74530f3bee116f6d30aa27bb83769f1ca090d176fb`

```dockerfile
```

-	Layers:
	-	`sha256:cde878aeb2ad2a1d1ce007affbd6c348b68b94ea660375585abcbec555379070`  
		Last Modified: Thu, 04 Jun 2026 18:06:14 GMT  
		Size: 5.1 MB (5070553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca700f7eb3f536cf7328db59f26c6311b62c5f1337c408a3efce048bd07a9c9f`  
		Last Modified: Thu, 04 Jun 2026 18:06:14 GMT  
		Size: 16.7 KB (16739 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e4770f94bf5f5979880ecf4c5f2d4d70bca6d5ea7491995347ed9294888cc4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180762453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb0a35fca58736f57b9cece830b3e76cf47a62158fc1ca497bf978c2265a05d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:25 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c0d978937852c41db594ffaab6cdf11f8a7c0e6489637ecb3126ae425f9dc1`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6e019f67fec744a7096b62931f60dce935b50c1b884c17098f4dd50a65311`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 65.5 MB (65452492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9790596fc1458c03df847f74212754b33d9bb4de77ddf364de3b2b36cd90fb2`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce18100210fd99f083e0c50b574a1165e668e7dfa37bd40e9668683dced8c3`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80f2dfea8bf2a41769af837d2508ac78dc41300c36ad7e542c9f1285a6fb1244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d221beefa97f597dd098b8be67f5eb8c1452fa1d5cb27ad5e3553b963a36c3c7`

```dockerfile
```

-	Layers:
	-	`sha256:ce081d055e74e3f1dfe512b828990a7130eb943c6c4053429c38ba7f416e395c`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 5.1 MB (5057954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5232c337f843e62ac6bc3edaa24c6b0f0909d6c358171dd429a106036b8cd4f4`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
