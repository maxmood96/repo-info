## `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim`

```console
$ docker pull clojure@sha256:8f6709bb99327fd192363a921890d20adea224f4f12e4ee5751ff4c51bb6bdf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fa720c50dc9d39330c20a4e4459a16cfc600fa68451b971da33fc6f0589301e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29583d66ca42f4b4489e5ffe547c5b8858d9d73fdeaef715cdf80683ce6b7a11`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:21 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b907d7417180342b0cf27708e33be1026b729e843c213f71aaf9b477ae2b8ce6`  
		Last Modified: Fri, 19 Jun 2026 02:22:46 GMT  
		Size: 52.7 MB (52669121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b28ad8dc3254e4272dd73c01f7b2af438a35e08073da3fa0b26f593f1d872`  
		Last Modified: Fri, 19 Jun 2026 02:22:46 GMT  
		Size: 72.5 MB (72476158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aff38e3f6b0cb51ef8e06c370645444038202b52b922f0d1f41d83ed9f83e0`  
		Last Modified: Fri, 19 Jun 2026 02:22:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dcabea9b9a4fa59ac2b7308cca102cdcabfa212bb97a889887a87910a0e58959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003cc742d3ceefaa061a08524148cd2d7fd8c7a9fac2c53d76abe1495c4342c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f7c6eece09ec2163e50dd388742f3947bf2d0915be0c921824741fa3d5d9151`  
		Last Modified: Fri, 19 Jun 2026 02:22:44 GMT  
		Size: 5.2 MB (5240112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5c313053141bab478a14701f68d95e00a1d60c0ebae5a89fb73a3051b7d1bf`  
		Last Modified: Fri, 19 Jun 2026 02:22:43 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json
