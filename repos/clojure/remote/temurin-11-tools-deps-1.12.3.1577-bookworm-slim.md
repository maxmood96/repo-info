## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:880574bf8e63f78b901f57ffc349c538a10acbc32c9b15ebbedd5a4324aab771
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:09cba0724c2382195c5614df2754e470c5c08a4dd4ec2665df3f46e54d88f7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242874985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed43a4005fb36b58bf3894f06554386d903edc53092343655d618148b835933c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:51:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:51:33 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:51:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:51:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:51:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f42113aec77f60e1ab76859aeb124f8d0a1077d150190dc28a8d4a25b0a08`  
		Last Modified: Mon, 08 Dec 2025 23:52:30 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e6baf8e4e7a4dc3ffef2cd19132fd91b898d5c4e70aefead3de699126566eb`  
		Last Modified: Mon, 08 Dec 2025 23:52:24 GMT  
		Size: 69.7 MB (69679273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b27497cd2064b4ddf50846a9535f62f4ef6588284aed30eb6f98a7df397bc4`  
		Last Modified: Mon, 08 Dec 2025 23:52:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af2ef5d4ebfec6dbc9ce424f5a9f7d3f3cc6460cdfe38ed11b52b57d458343c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb63e86b442b78a2876482e03183b951e579e1eb46699fbfdd099743850b1255`

```dockerfile
```

-	Layers:
	-	`sha256:2d71b43656273f8252cd6e4136690a5284b57203e67392b7949d799221c525cc`  
		Last Modified: Tue, 09 Dec 2025 04:36:17 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5165cc684875c171bcd8cbf75cca98a23a4102def043d137a2bbec15e415165a`  
		Last Modified: Tue, 09 Dec 2025 04:36:18 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06f20c265755282e0d5c44233c76868442b6e22eddb50b8016ec817b47538606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239394856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59e5866f284d976b222f9dafcfa5b315c0aa84eee463f8ea64417a34b58d9a5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:59:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:59:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:59:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:59:51 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:00:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:00:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd0b703b31390aa517e2c9fe502c8c46e6c54e6a4b7c770b7dafe361f7ff8db`  
		Last Modified: Tue, 09 Dec 2025 00:01:00 GMT  
		Size: 141.7 MB (141731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3cbb9f8a352ea9bada266cee341aa3e16c2b075cb0c302569309bad8f4a9d`  
		Last Modified: Tue, 09 Dec 2025 00:00:58 GMT  
		Size: 69.6 MB (69560422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8231878262ef82dbff91dd6a8ddfa051a92b00786337fec7449e82085c9fa582`  
		Last Modified: Tue, 09 Dec 2025 00:00:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e8b5cd4ae2be6e6fedf3a426733e7edfa3333fbf3b458f91d8c3eedaca486a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460e96b810a06b4b475e8418043f8c733cd56e910f62fe0c586401d5e54e05d2`

```dockerfile
```

-	Layers:
	-	`sha256:91a054169a56a9213ba7ccb9e676226bba1c46c481212b3ed5a7319e9994aa86`  
		Last Modified: Tue, 09 Dec 2025 04:36:23 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9c86eb872e418793f3f4a0a052a770f584a92a50d8bcd86913d7c344d9e17c`  
		Last Modified: Tue, 09 Dec 2025 04:36:24 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6f8dfb5b4b8f29ad8a84a26f14ea0b343e7479ee6907a3cd6e11121dec1b6985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239665332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c688ef1bf5de34eb92889fe74859edb91bba45b5d2f06c85d6572a9426e7167c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:17:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 16:17:17 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:20:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 16:20:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 16:20:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4470482a8eaaeab4dceb8ce35bb823da20ba2a67978f6a17163d36b3afe2763`  
		Last Modified: Tue, 09 Dec 2025 16:20:08 GMT  
		Size: 132.1 MB (132081995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea2aa5c5b236c235611c6a8172450b74cc3ddff24693e8309bfa123e9e71048`  
		Last Modified: Tue, 09 Dec 2025 16:21:42 GMT  
		Size: 75.5 MB (75513845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f471c9373c2d1cf6b67b9b9c62f758247d735e491b9c74ebe524b9c41fc7c976`  
		Last Modified: Tue, 09 Dec 2025 16:21:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c97ab780c472dbb79782c02d603f2cb75f7ccd3c752cbc7635dd86e623853448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a25c54788a2f2640bee2f435d245b49246d51f886250cec55b052bbc88ca14`

```dockerfile
```

-	Layers:
	-	`sha256:d2971ccf697b687cb7a4a260b5f4a3b2c98805ae90947e8406b8e777f88750ed`  
		Last Modified: Tue, 09 Dec 2025 19:34:50 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3507dd5c71d9214aadc916c56f8fb82b42581e0bf0f73c30197850daca935f14`  
		Last Modified: Tue, 09 Dec 2025 19:34:51 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:04132d2d7497ae0259ac41c27b9d117d94628b9a8ffe99de553de5a5814bdf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221070082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c0cda96f9297b815b9f769e3514efec858b5f95d514c703ee9dd152c09b707`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:26:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:26:21 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:27:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:27:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:27:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a89e0d855a144c8a937b507bba42121108ec2b59b7e013828e537deaaa8563`  
		Last Modified: Tue, 09 Dec 2025 01:27:18 GMT  
		Size: 125.7 MB (125694469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeb082b5198a59865d0b77faa8b770d1481dc97a8469cad9c3187d06b982e2a`  
		Last Modified: Tue, 09 Dec 2025 01:28:17 GMT  
		Size: 68.5 MB (68490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653973d4755faa2c150031ef1f4547163fc26f45886d25bb0754c7726595d054`  
		Last Modified: Tue, 09 Dec 2025 01:28:11 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62f059598753155487cc1ce55132de8baf4e270843a7864e9a939e0c45aac8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a622253a653dbcc3e2d67482869430533aabef279b7b5ffa45cad7d19ba4298`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b10017b5adb9641c4378972df6b388ad829d16eb8ba3eb452bc1fe0dae2bb`  
		Last Modified: Tue, 09 Dec 2025 04:36:33 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0db27a1101758c5ff35d53a75a55c9422937233d5c0c02039ae9aee78e7a44`  
		Last Modified: Tue, 09 Dec 2025 04:36:33 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json
