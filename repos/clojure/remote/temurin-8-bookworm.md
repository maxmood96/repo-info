## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:6ba5713b8ce3421fda2dd3cba8d03853b04020a21145187b5908caf66d789f8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de47bd2742684151638ef141e437716f390be081c395064d2445ea5f68855080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234148358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbf3a4729046b00c79983db9046934abb87da147f32e728782ecb0e33f0c832`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b16c04b8f6610e712af885756fd98e57967888b9edf73edf4f43258092f2bf3`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 103.6 MB (103633891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c68e003724c2587778dab1ebc3619061532957a80106c791426cdc10bce55b8`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 80.9 MB (80938131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12b9eae06f9da6e37ade0f7182d8e55816865b804763fabfa679ef6b794cf1f`  
		Last Modified: Tue, 12 Nov 2024 02:22:43 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9a7bacae4fa476c7514ed3b1ba9c6e2d9f6cb23db4f58293772ea48b08e3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ba1d51996ac1e9ee81e7f2c7df93058f9eece9c8d6a627fc495d03ac756768`

```dockerfile
```

-	Layers:
	-	`sha256:411f4981dc6778dbb66a1740b5dd9b01efea42f1b472cfff2d18091e6a8f3cb0`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 7.3 MB (7304593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ff125719430986dbbc79b1b63c4ebd34a4ea42acc626c952aa6da4d6c28706`  
		Last Modified: Tue, 12 Nov 2024 02:22:43 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6703a08ab10c45cea247c42e212bb8f372e224000055ca1b650d5a280dcc017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233133894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218624a6937e376c75a91f922990c6fb623e138e5a1920c772ad72a01f9bd7b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98073152dc0a36893a12799a586412c57c2f3f68a2a1077807c2ac7bb8d22bd`  
		Last Modified: Wed, 13 Nov 2024 01:01:03 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33790911465edec5971788d716d2d1694c1d9ba787974edb27dfa742057d3456`  
		Last Modified: Wed, 13 Nov 2024 01:05:26 GMT  
		Size: 80.8 MB (80798335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0579ede4be89928e1d65da294f05d22a039f9829636269dc87b5d26b87d33daf`  
		Last Modified: Wed, 13 Nov 2024 01:05:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5dc3d1b8d9ce76e19384c65f40dec6eaaf92f32c5e4bb7233023ae00db10e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7325420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e174ea32a6ff25a9d18abec4387a09b317d5953132df12e2fb1c03999f8f12`

```dockerfile
```

-	Layers:
	-	`sha256:8f7e00a5e5b80cbb9a77e8b5d66d9c36f4ef90a289bd33707863d66191f8b735`  
		Last Modified: Wed, 13 Nov 2024 01:05:21 GMT  
		Size: 7.3 MB (7311060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daef6f211c67ebf70696a86e9246a90ce88b3e1f206f8a2e92181e6fd61cc02`  
		Last Modified: Wed, 13 Nov 2024 01:05:23 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
