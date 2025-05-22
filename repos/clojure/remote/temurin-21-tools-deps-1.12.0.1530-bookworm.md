## `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:ae46f6ddd99fab5b4848d121d1fee908795c9fa841ac6ede39e12a05ee348037
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

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ab8e08b3462eb568efd3de8029b0af842b8a6ad4cba0e4d3bc887284cba3bb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287118787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956cb45583e532b1f7f71fbd7da04f5166b9bc2ae9ab64fad0a3e2b3ec3cff0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d1afb00f146e0fc160476d5cde2ad5b8999b87027f42eb4b8fa179ef3513a`  
		Last Modified: Wed, 21 May 2025 23:33:34 GMT  
		Size: 157.6 MB (157634544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db15b35aeb2bced3b8bd7fbacd7d14c83f080ed5c01d5fce04a5c55203797f9`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 81.0 MB (80994957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c76aea78e9d309e800732899d684a81028b91f00d13e4bd4251e2398e1422`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7505ecfb1f0ac6936241b66cc1eebd1f1a472cc74345c6552609992927d2ba`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6d090e11051cb6431d568ee508b57e4a006509e570d15e3d08619bb8f81e6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529b840f1fd0cd38ec17db47b4625a91863a2f035b5de8b97fbb85c538103336`

```dockerfile
```

-	Layers:
	-	`sha256:1ca7afb0e7a95cfc0185179eec1f7cb95e3a6a6204ff6b154df53d6a9207ec4b`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 7.2 MB (7223624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c70a1f8dc38e6e1df871e663cbcb62a0c8b0452d66c01202b783d1b1d149d`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03cb0dfe9efd242b8f63b3ac0f21613a12ef6d2cf5fd16d11806dd7691b0e102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285103987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a072c36b1bdc7c87d2965c86be60905f1bd36146487c137eef3eea35094959`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f670fcdfa1a1eb797188a5b4ca5053a8314031c8c9ccafb10f28c17b8a14294`  
		Last Modified: Thu, 22 May 2025 07:59:11 GMT  
		Size: 155.9 MB (155928835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f10cbb3e519a9dd78d7659ddeefdef904a8dc2444280ae4e30c178f931da7d`  
		Last Modified: Thu, 22 May 2025 08:34:17 GMT  
		Size: 80.8 MB (80846930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec04a8a382772611ec75f31812cf134119972c8893cb41c89b35191f5db646`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee410f678ccf2cc4d43a56c85bb0091bd05c63fe636ea4480b2050d3314a7ed`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:94152a273395c5406ee9cb2f9bd09b2927bc0cab261066c5b50ae1ec159c730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771225bd5990814e63299691bc856a81e5ca0a9fc39ad7ff0f1c175aa866f80c`

```dockerfile
```

-	Layers:
	-	`sha256:c44363d35a22682556f0ac86c6579753aee9dd51fc5520f17dcfa50c9506da68`  
		Last Modified: Thu, 22 May 2025 08:34:15 GMT  
		Size: 7.2 MB (7229459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3aef58842b4d74672d0cdf54a441c60c0156c6f26a72344124cfbda6aaa5acb`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:720039d0ee1924c0ce6f73be13cf5fc04b9cd73dda2b20f123a447a1a1b6d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296938623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb7b84179a27dff1636ffb5b5dca39535c2582ee2530543970f4b3b6f3c30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc318831ce756576c268e9599222761fdf41dc94981f81f41b532a8b7e7e22`  
		Last Modified: Tue, 13 May 2025 17:55:11 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e2881473afb93a309b45e7e901091230e378c7f327a66237ac2a00fa40a8a3`  
		Last Modified: Tue, 13 May 2025 19:20:47 GMT  
		Size: 86.8 MB (86800546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ebd6b4d18d5cd14c4299684b53f831bb7bf7f1fb6d637b2655d5698c0d566c`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc07670309152a23b30266e4291dae7e6212840c1bfe809760fad96dad9a38f`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:530dac63eb6a539e334f56e203faa1742577500037f164ae8a2812b8348afa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d6630d610dcca7958e9bfd8cb3337b2554c9b9f34be0ea1a67d477e4372f58`

```dockerfile
```

-	Layers:
	-	`sha256:e29dde749e47838773b8aa1e4e66fb8888767b177a7433906345c7ddd87df081`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 7.2 MB (7182656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2152386538f966ee3589a97e478ca204d942e80d8e1247cc49bc39fd37a9eb`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b46aa39c0afc739197493ae74f36384ffc6a6f7e5d27671b5faf43e963308ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273845873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba67866234cf4b0e338cdba880ad706db28b29b7eda9976b4bc2187e2731d2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f7f624f9251dfb21473d25e67300bb9a6b55ab2e666b7bae6f6bac57d4456b`  
		Last Modified: Thu, 22 May 2025 03:37:38 GMT  
		Size: 146.9 MB (146910901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3647f48d61b24c50c3ae5ea62903620c0b19d0054d7e63047c4cd50a8bc4fd9e`  
		Last Modified: Thu, 22 May 2025 04:01:31 GMT  
		Size: 79.8 MB (79790091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf05c14c77bc058c21f858c1a1d189b72cba0a7cb3f9beb81fc39370cd189e7`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9cf1844c802b0b6d329662eafaa4467c40d9695bc045189dff29b73c4a60`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a756c68bec3f3dab309ecc5b4db0961ceb8298838f5124e03ae09118861aeb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9c20c3088d890fd72dc5452e99e8014ad656db302085e2622a4fcd68699a53`

```dockerfile
```

-	Layers:
	-	`sha256:8577843467f779943e13719c99cb3d1ce18fbbbc249389b27030e3c17a4acbbf`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 7.2 MB (7217835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216b9466632b94e04aaea541f2456c6b18e6e01bf562cede591fbded3a38c9e2`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
