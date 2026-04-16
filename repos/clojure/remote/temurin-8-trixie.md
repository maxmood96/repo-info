## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:3b5e0e8b1568c1e609525b6455a4934871193fadbd3ab8564a7eab15c403a1ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cb4d1f0163dd0627efaf4b1397473f6288173d9bd04f750ff58bd78e8d6d4a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193550432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8eb91cc6afab59a5223407fece8aaee42c3fcdd37f05f5ca1bd8715a76cc7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:51 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:02:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099a692a58bfd49ed8958f65483bd10fead8c0f50ba4bf3b09ad4cfc70c64b1`  
		Last Modified: Wed, 15 Apr 2026 22:02:30 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97028e3116a8423597267859563c194a2ec4e717daa1f13d8dac27effda7c30f`  
		Last Modified: Wed, 15 Apr 2026 22:02:31 GMT  
		Size: 89.1 MB (89081835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51f69a4caa30723b9e8d358fba73332d18ef0f3a2a73f87a6c06696bd363ff5`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e65a7cfd4ad6b314b8ab3b29f5cd5c1d0e1a6f926109de7d73dccb1389b3fa61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7d817a06ef8139e1b622c391d02e9d22425b79f162a1bdb414babaa2954860`

```dockerfile
```

-	Layers:
	-	`sha256:0a2850d47428446daab0b84e7119fad5a6d58ad25ab8e3374b69f2f530088d36`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 7.6 MB (7591654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c663dfda8fe30789c38d217ccb4b902b73003d8459313d01ce2ef5200252bff6`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bcbc6636dbc9c161aab6536ba8a2043c44ce9a839c30af870523c106a20acb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193171093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643f7ead4dc7e9e35ac5acc4cf40a1b443fd7a13d26cf751cd5b547530989955`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:13:11 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf693ce8c236550ab90c4e8ee3d7beb1d36d69f546df4761abe09f7a5c3850`  
		Last Modified: Wed, 15 Apr 2026 22:13:51 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0b5165af493d77a264290f94ee27b7aeeabc6097023f3a38c3f9b6dd4c69a`  
		Last Modified: Wed, 15 Apr 2026 22:13:52 GMT  
		Size: 89.3 MB (89253578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98178115b498b56df388081aab61add9ad134ea28ebd2ecffbc8a99be512b45c`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ef97844ea153dd182a0e541da7f61b8ae4704bfc45b25f6dac4ab90eda1310ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc87b5dfd918708b7b6b850cc56e97eb1bfb58eafc933dc4102ccd5eb72e96fc`

```dockerfile
```

-	Layers:
	-	`sha256:8e91262894b9d6b6a3287fa8c7b67c2d923f069c725b6e5bbf8711e0472987c0`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 7.6 MB (7599384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba405ee012c3f240e0126833a66360cce4c3a08da661feab6d17f35b54b81642`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:585b6153ea976d96d2ebbe18fc65433e4a9e8fae3bd3206692068888e76fbb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02367836b950962be2a6f32b7c0b907917659ab9933fc3647171df678e5a0ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:22:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:22:59 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:27:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:27:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:27:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de41bf7fd798d7a67da7d6002cac62ec5cd96ebd90175ee55ba10334fc7bac0b`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 52.7 MB (52650418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d160795cf5df69816961ebd868cc2aa8959cd97c7261e91e96b4be2d881eec`  
		Last Modified: Tue, 07 Apr 2026 14:28:17 GMT  
		Size: 91.0 MB (90987356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e3f91d0fb4ca981525abf535a2c2437321c48b7b372887a9bd887b88a6ab02`  
		Last Modified: Tue, 07 Apr 2026 14:28:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c75087e540c672ca60fbe1216d755832438abd9f6224bea2346d2ffc5a480e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a4ac794371413a8abbb5984f1e5f0d040bba14b7fd43186925854cf33597ea`

```dockerfile
```

-	Layers:
	-	`sha256:5403b9a7e5bf42eeb6767b8ac99c50a9efdcc868ea72303347eb91d5173ec472`  
		Last Modified: Tue, 07 Apr 2026 14:28:14 GMT  
		Size: 7.6 MB (7596670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d624ece172b19161fc42181b25aa4ce30c1cb8e293896b66777688387a3d2f26`  
		Last Modified: Tue, 07 Apr 2026 14:28:14 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
