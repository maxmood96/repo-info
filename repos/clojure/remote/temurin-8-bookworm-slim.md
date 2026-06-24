## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:9a6a1bd77af94f37d5cd11931e1c64f47099682eb5602461b0056fe866b9539b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9de694ca012e2320246151a543612640f8d25783f42240ba332c0bef26dda5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150079917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33eff95685765f004cd41b5626825476d099692a68b87252e93653cd5389443`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:14:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:11 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:11 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:14:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:14:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:14:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5c29e7ec0120670cdf911fc62db8a297576e413e4346ba40085bec884f01c2`  
		Last Modified: Wed, 24 Jun 2026 02:14:41 GMT  
		Size: 55.2 MB (55198699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad558803e26c5e9a517d599f64973d2b1789dfb3bbf1980eabe3f304f2923e9f`  
		Last Modified: Wed, 24 Jun 2026 02:14:42 GMT  
		Size: 66.6 MB (66642935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544257ebbda89a22010613bbff68d2c6430f3f567f56fb39e8d4fe473db1391c`  
		Last Modified: Wed, 24 Jun 2026 02:14:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3bd7be20df0c3d0c746190c301e5313065ea6e5052d603b0098c7a8b89fbe46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba97f0b1d54b0ca6da3012b8af24e43c84fe7c07a02191680d923daaa5b6659e`

```dockerfile
```

-	Layers:
	-	`sha256:efeaac028a0d499a963f05473981ec30d7a6b37c88abfe4356123c0475d7d245`  
		Last Modified: Wed, 24 Jun 2026 02:14:39 GMT  
		Size: 5.2 MB (5234359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af07364fad7decaf2f8fa8694cccc22692fb73937ae8b340a914c29cb3d3646e`  
		Last Modified: Wed, 24 Jun 2026 02:14:38 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b63ac9c619af5780834b71a5f0945bfd804f5f984ee854af0853fc9280cc7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149039404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8970dabb4f1c872e086cc7db1c1867e18b082690148ef704e61762e62b704`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:20:42 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67296079b28c13503764387991a9d07831cfa25f16048742e7f94c79eb938b65`  
		Last Modified: Wed, 24 Jun 2026 02:21:14 GMT  
		Size: 54.3 MB (54272921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9fac62ae7c4486db52b3f1d669e595fa6f66641cb31ddbd0e00cfb2cd9b7b`  
		Last Modified: Wed, 24 Jun 2026 02:21:15 GMT  
		Size: 66.6 MB (66643420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3a1f3f791ff7841997c03c685b2fab07f8dc5b55029c1b5e6361224e5a279`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:400fe5a14e972f2c5f18aa0c54c9eb3d07c34995e771396a473bd5a06a9c32b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085a064e4fc786b56a3a6930c7bfcbddc184f3cb3e9c270188c911999121773d`

```dockerfile
```

-	Layers:
	-	`sha256:e72dfd449d224ed1c7432dd305f657ca87aa16a1c3061fdfa92e13f9b4a26cea`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 5.2 MB (5240820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84003732c24ad8236668000c8ae489b6c9fcff5acb8aec96f7f4aef8653c0ed8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d69c6443a83c4637d1989402f89289e68a2fc7baf34e67536f46ace4bf35828f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157228060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d247708b4b99fdef7650fe9726054e43ed594ba5aedd0f5c287058ce455629ee`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:48:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:48:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:48:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:48:33 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:49:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:49:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:49:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31e72ed186231dd5cb2d9bf904909eab694033958cb028c19276f67c42d9c55`  
		Last Modified: Wed, 24 Jun 2026 07:49:44 GMT  
		Size: 52.7 MB (52669118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788642e9c0d9a309d452ec8dd6f071fff37025f68d358c8c21e838cf05ef321a`  
		Last Modified: Wed, 24 Jun 2026 07:49:44 GMT  
		Size: 72.5 MB (72476321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40a37a717bcf9a7ff7f142924bec12940d9f8d8cff40c4d7a9b858f73131dd1`  
		Last Modified: Wed, 24 Jun 2026 07:49:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8279c09b7738cededd2d83282e2e5fc6f33376f958e7c9deb046c63bab9c5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f36503df0d8e248a97926343b877c0816406514f94ad229726c374e0e34a896`

```dockerfile
```

-	Layers:
	-	`sha256:eb64c380faf75da490d873c2e9ded3961517fd6637274e849f653dbf01f2b03f`  
		Last Modified: Wed, 24 Jun 2026 07:49:41 GMT  
		Size: 5.2 MB (5240112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c56f9970a31ffff0ddf61ac449f20f0e1d30229135e9feeeb8ffb62148ef4a`  
		Last Modified: Wed, 24 Jun 2026 07:49:41 GMT  
		Size: 14.4 KB (14450 bytes)  
		MIME: application/vnd.in-toto+json
