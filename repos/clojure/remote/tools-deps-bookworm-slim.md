## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:09dcdab2355dc8abb2fccdeda606b50aa3171612367d886d25032a71346894b6
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:994158db4e86d7dc8d059e947be456f219c5c8dcbc624417359202a148834054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190195007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af24e19f75d88412e222c0a6a940580bd9bc5a4bf33b541018c38cfc0cdd55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:36:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:31 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc20082dab795c4f6bfd2fb431338d3734f0624faa22bf55f781b5fb40bf4ac`  
		Last Modified: Mon, 09 Mar 2026 20:37:11 GMT  
		Size: 92.3 MB (92256298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e5eff05562c1aad085fe0cfcfb7a72adf46f8761b1a5fa5770d7291fcfd07`  
		Last Modified: Mon, 09 Mar 2026 20:37:06 GMT  
		Size: 69.7 MB (69701387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0d65d30bb63a101a4afafa5c6d28ea85fe2ccb2569ce56c0b55b51c7a03d`  
		Last Modified: Mon, 09 Mar 2026 20:37:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25af8b5ad3922fb6546c3dd9ed485e60cba3879dd85d62f663c715a9dc1437f`  
		Last Modified: Mon, 09 Mar 2026 20:37:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6e1cf7cb952d4e2159bf41a722525f41c3f2174f75d7f62826516080c198f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a90c4fe188ce9a9479327505a39a35bfa6aad10e98ed0f746ae070f4ec9e7b`

```dockerfile
```

-	Layers:
	-	`sha256:d6529302ca6de6efe1621fefc27103fa95107fe0118e127f2a0361d9ccddc566`  
		Last Modified: Mon, 09 Mar 2026 20:37:03 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c366a8b6173c47fe715c6e2347c3905dd8a59f63db0009e59f1f4c8bed6c427b`  
		Last Modified: Mon, 09 Mar 2026 20:37:03 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62bc46f85d0f2d449304a323bff7f12959a787e87e8cf991a656c08fe6ceb7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189094548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1244b9d210f758822b78ed963a4084b7113829159dd92b1071700f58a7e18d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:33 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f08e94a24425ab62faa58acaa8c7b581fd05d8945b788792bf8e3434087b5`  
		Last Modified: Mon, 09 Mar 2026 20:37:09 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849bb46af0ddc2aa429d0bc1ffb4431054f68f4b054839a8b817f18fba040804`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 69.7 MB (69689162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7938feaf875ad4ecfe3c560756dacfb7966cf0dca4dba935317de185e6010737`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e446464ab118e16a167b3fd75107549c0f0694e7551639fa73eac9d0a2f055`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4659aac49c547ab59a749e3befaaf0cf3e5a2a48c2396f054d58ff84aaed52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f744ec25d37e90eedb55fea02bb4825ffd8ab14df1ee2f8cd24bf79bc6015c0c`

```dockerfile
```

-	Layers:
	-	`sha256:a93645c2d46e69885b177a09027bcb27d55eecf5abec22b4a59d963663e27c10`  
		Last Modified: Mon, 09 Mar 2026 20:37:06 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c1858e4bf6a55bf5bbdf1e1861eeee1fe325bbbe7a4313fa312dc40ebf4f8f`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b46b66193e7719800521df80db27c9fda0b95a75f670f4eb308b85be20080111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199245903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed44b9aba5d69153a55a24ea4119de94cce0b19188849fe3d2a179ba7a924db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 21:06:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:06:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:06:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:06:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:06:58 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:07:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:07:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:07:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:07:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:07:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0593f8e346e60f3605e0b67dafc48826b4de375b11a97273e5c663d7efb0d`  
		Last Modified: Mon, 09 Mar 2026 21:08:39 GMT  
		Size: 91.6 MB (91632879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d68bbaa66614c37225be15e533adb6959902d5b4ff53bea3af88b6d8d14258`  
		Last Modified: Mon, 09 Mar 2026 21:08:39 GMT  
		Size: 75.5 MB (75533646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd32604073580bdbf93b502eb0d9c123983c56ce18b76550fbe0244baa7145e7`  
		Last Modified: Mon, 09 Mar 2026 21:08:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119c216841b1df306784c34415ddf48fdf88c8d7b5741fb766af060b8db04175`  
		Last Modified: Mon, 09 Mar 2026 21:08:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:139b68524961a2ea7279e4a2ffd0d310c9fd8eaaee42859eb48ead53361451fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1662353272844250ae5b8ba8ca0b20b902139b2cd254fabac223de6a89d25e43`

```dockerfile
```

-	Layers:
	-	`sha256:a12672a58846c8d385617ecaa11412756e183972475a4717c4996e70c9675f46`  
		Last Modified: Mon, 09 Mar 2026 21:08:36 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc46b13b0f806f585f03a5c63a5bfc901ba330bb0c78c3817993cb97f0419fac`  
		Last Modified: Mon, 09 Mar 2026 21:08:36 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fecbceb7858a363ae1b18b9e52a714f4562db28f8740e687988cbe27b5a40547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e35d4c843587520fa2bfe201430eb6bfa95092ee52ba16205affb3792d3a71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:37:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:37:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:37:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:37:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:37:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:37:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:37:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:37:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:37:38 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:37:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d53f2d57ee0d04bfc74686920e0d427e0906984389f40df24c83dfbbb6ef91b`  
		Last Modified: Mon, 09 Mar 2026 20:38:04 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e1b32036a986e91a2b8d3fc9b6cba4e7e6e691e8c6725c66c741c50f70cff`  
		Last Modified: Mon, 09 Mar 2026 20:38:04 GMT  
		Size: 68.5 MB (68513640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d65fbb51523a03450590920af7ff01a65f482d1cac3b42a5eae81dba66a84`  
		Last Modified: Mon, 09 Mar 2026 20:38:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d28f11d745bc6160cb5519c681df1fde080af2dd3c5417ebd5b8aabe31912e3`  
		Last Modified: Mon, 09 Mar 2026 20:38:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58847b28378815a21107d310a93e8d30f4b7576d381dbdb028c22c2d5be8ccd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0fc4f487a558718bb87c414d55b84e6d928d060f04e957fb838745c955aae`

```dockerfile
```

-	Layers:
	-	`sha256:2d4e62c09fa673f0a4a58df9a18e813ddbf85ab6a67eaebe34a4556da01ea765`  
		Last Modified: Mon, 09 Mar 2026 20:38:02 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff38cda6e023d83c32b7a56ea43dfc466903498fc64015501328628fb980727`  
		Last Modified: Mon, 09 Mar 2026 20:38:02 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
