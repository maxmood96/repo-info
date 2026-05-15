## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:3595e251284daec31bf4fc9f557421fe79c64d63151e23fc1d48d772d1f820df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4f36eeaed7a0ec7155922aaeefc251482587f98e4cfd0583fb336d4b9ead4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184901800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8988db4eb50cf7a882f05341dea3ff330083af9442e0bac5d1d579a239f1775`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:40 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:41 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22356e8825515b59060ba8748d262d28536a06366e5696448f71bd73ff0190cd`  
		Last Modified: Thu, 14 May 2026 23:34:14 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e481684f8006454aefcfa470d8d55d1d9806d687b28569021675898b0463dc45`  
		Last Modified: Thu, 14 May 2026 23:34:15 GMT  
		Size: 81.2 MB (81213756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa5755b38bd8123db7eb845b2390c5c08c55c95172cd232baafd2a05c7a9d21`  
		Last Modified: Thu, 14 May 2026 23:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3df0ee90738c09e66a1cbb26ae4e9169a8a5d988cf6ec675a399c10534347b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c87e6dfc17cebff793c53bce70f0fb7d5bdb65e3fa9d5d1bc73b552d8593776`

```dockerfile
```

-	Layers:
	-	`sha256:b34eb6f4b76ed24345f1335deb506dfabaa30cfdc7ec874a7d3b5b1ac32329c6`  
		Last Modified: Thu, 14 May 2026 23:34:12 GMT  
		Size: 7.5 MB (7499287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d252dfd70bad05fa15d6ae697e3f88756d79ec7ca9968618ef5df5670948e58`  
		Last Modified: Thu, 14 May 2026 23:34:12 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:517eba6d234e309cc638fdd0b1770b0eeaa6181e0cdcbe0f5837f21055b1ad63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183843790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3313b5e9d954e4f6fbe7a3edff25e48541ffc4d5affe7c966e97535ab26a7ba5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:35 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:35 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831d99cec7e7a42d93411d04540d01e3fc2fb05949a91789a0601cc421daff6`  
		Last Modified: Thu, 14 May 2026 23:34:08 GMT  
		Size: 54.3 MB (54272903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed7c2f09b2095d355776a4c329840aa2c8fb7dd158ddf19d09f052efbc9161`  
		Last Modified: Thu, 14 May 2026 23:34:10 GMT  
		Size: 81.2 MB (81197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb57778ca338318aa6130ac43c483cccff1bde6f36a652d37d6bec1da84f37b`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cedcd5521211ef3bbc433575909577569990e9c6a1583e596f3f3d8912d20cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304acc1edabf6c740403c6fb36f97a0f1dca9e17fb1bff7317029acfff35b518`

```dockerfile
```

-	Layers:
	-	`sha256:bc4b2584826ee67a2933892bb82984bbc5bc8dde05d3305c49c3285d548e0252`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 7.5 MB (7505750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b167cfbe2d355ee3601c1796e8dfe8a176b4908cde99f76f254e218354d057`  
		Last Modified: Thu, 14 May 2026 23:34:06 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d7a369d6eca728ba78fec0a5ad35ef8a1cdbe86f556eea4bc0db799c328a3cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192040033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6051520630f0f0977ded694054f7e392c0c713b388323d006b20ee86279f2d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:32:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:32:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ae6c5cac713a69400cf84432f14c7e287e227f8f9303c79b6fca45c4bd3f0`  
		Last Modified: Thu, 14 May 2026 23:33:28 GMT  
		Size: 87.0 MB (87033447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45195a4ac1680f0cbba682ca2f8c58989ad89a2dfc609974c1e0574418a6b49`  
		Last Modified: Thu, 14 May 2026 23:33:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:da2be9c1e70d061bf92088a9e79f338225219d0639f4e7684287dbc613ed9cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76752cbdcb2250435e6cc451635fd98fd52285b85609b6b6b5da808e25eaae3c`

```dockerfile
```

-	Layers:
	-	`sha256:9e48b491e22809f653e73ca93aea9fb369701a8412cd47df87cc9fd7e91e9f7a`  
		Last Modified: Thu, 14 May 2026 23:33:26 GMT  
		Size: 7.5 MB (7505098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20612fbd4626df96e83403cb0f3a202788eb59cf15647972c3f98a3b86d29af`  
		Last Modified: Thu, 14 May 2026 23:33:25 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
