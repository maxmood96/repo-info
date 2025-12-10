## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:915c8a82846335c876e0d0a03df1fe17a2a57f8982d2d8213987b9479355cf56
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:78246c56fc6e28e2d85d32e64a8636dac18b5df3148465a38bb4d1a73657d66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255734526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a65f626ebd5d1d9b29ae4334a26d004796ab599daba7d8fbabf91db2df039a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:55:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:55:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:55:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:55:06 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:21 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497131a10d6af5263acd58f770bd57c58c982b55c5271d35b7bee259611b0f9`  
		Last Modified: Tue, 09 Dec 2025 09:08:13 GMT  
		Size: 157.8 MB (157826032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd66f966c450a274c71fbc8da325333b5a4673013a2e69464f9cce24cd7a457`  
		Last Modified: Mon, 08 Dec 2025 23:55:54 GMT  
		Size: 69.7 MB (69679038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0b73ab3887a95b486aa1ed8f9c105c90e46df989ec5f277b48adab4866212e`  
		Last Modified: Mon, 08 Dec 2025 23:55:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b41ccfe9fd1f41c29a4119570a7f5cafa8b0bca47324400d66c548683e2a08`  
		Last Modified: Mon, 08 Dec 2025 23:55:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d62601d1e1f5cf1135376cf91b14a666caf77baaa52f7b10217a7bb8dc90cc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfc9532f6d7f6549ebc373530052038e9dc869304b0ee01445756e3b9a80192`

```dockerfile
```

-	Layers:
	-	`sha256:553eed052c4fe60a11fcdaea72641fc4878f46c4a4dc22685d2907a1d8114a3b`  
		Last Modified: Tue, 09 Dec 2025 04:42:24 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ebf56c6a4ccb10729a0b614d973a73e427788e765ffd70d420027d6d4b8b8c`  
		Last Modified: Tue, 09 Dec 2025 04:42:25 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e29a63cf242693febdd6dc78519182b210c8c8aabb255eda121c9704c11873c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253771412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d51d47fc93f1d1b9def56e76ba797b5fb85bb914fa1c3e38a94830c996ad130`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:02:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:25 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbb7c380cecae5810c7efb5e844783596d0cecbc7191b51fc61095334d032f3`  
		Last Modified: Tue, 09 Dec 2025 00:03:19 GMT  
		Size: 156.1 MB (156107637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8cb135e6be6dff15ac0aa090562fe0840d52a1b9d680c49960d2f307b7f3b2`  
		Last Modified: Tue, 09 Dec 2025 00:03:12 GMT  
		Size: 69.6 MB (69560509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61afa1745809863697b6e9dabbd5483e8c2e22c5d14978dc3de1be2b7c0da402`  
		Last Modified: Tue, 09 Dec 2025 00:03:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d9b0301f78317b38d81b6418c2efd6af76d22bd5a9a20203f44411ad31d6c7`  
		Last Modified: Tue, 09 Dec 2025 00:03:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f0b397a7578ae73aa56f23f46b6a9034e3ea80ec6c2a574456c896cbba889def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0905fe9382a5069128046554d93d81cfc225abdacf6f7166001fc7341f1c3708`

```dockerfile
```

-	Layers:
	-	`sha256:5de6fe067bfc761300a833718b9e7a9b1090e5694857af7bc647b1d4585097e1`  
		Last Modified: Tue, 09 Dec 2025 04:42:30 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24acd838fb6ccaf653528664d6e2e708ad313b24b5f6480a9d18443be6b1e59d`  
		Last Modified: Tue, 09 Dec 2025 04:42:30 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cebea9935b352d79815b894c9ef8e88fc6f1dc4168dd15611670f0878d99cc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3957f1d180aaa2e6cdc55a24f2a54c1c4aa2e1afef85a7a3eaaa8a65adf116`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:22:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 16:22:00 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:24:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 16:24:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 16:24:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 16:24:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 16:24:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d170adcd864f030aabc5ba607c417b8b9efd1bdb3b13f20e801de697b8e3a11`  
		Last Modified: Tue, 09 Dec 2025 16:27:29 GMT  
		Size: 157.9 MB (157942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f67ec5a7fcf9cb741be09208d5c97d0d1000968069f4d1420732fae7d65be1`  
		Last Modified: Tue, 09 Dec 2025 16:25:55 GMT  
		Size: 75.5 MB (75513173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9488bcf5d0b82fc65939d0310e1bdbf8d7288bd3f8ee0392015f030024e7097`  
		Last Modified: Tue, 09 Dec 2025 16:25:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3c378fd09602125036819bb78c4788c1186cdc2d6241d8efc017e1590c160`  
		Last Modified: Tue, 09 Dec 2025 16:25:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f8a98510ef2abf241a96a49a6cbbab432211fc68b0b592b980ad8d77caed1ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1efb4bdfd00ac43cbe2bac3385092560f25e8f3dd0ea8ad30b8c8297e0fcad`

```dockerfile
```

-	Layers:
	-	`sha256:ac46997862055d0702f80db829e06b6a1f16383892246e1ccc19f7004f7312ec`  
		Last Modified: Tue, 09 Dec 2025 19:36:31 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a566d2064542ad9a2bec40ac88d87c29407efa9f79e7766c1a5093ace8f67f5`  
		Last Modified: Tue, 09 Dec 2025 19:36:31 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ab8c9f9c1863a15da5ea9099014ed2351d129bd3f039a3bf23c6be03998598a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242445907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b53e67182862e4458314487ec61a0c6ce4bd8096dad6a8d34c0cc5c1340a3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:30:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:30:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:30:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:32:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:32:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:32:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:32:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:32:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa0de067223d3ecb4c513f6bcf0d76802a026b7899386bbea2d37a24c9a5ba`  
		Last Modified: Wed, 10 Dec 2025 06:09:05 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35670e8fdd515310af8e88e218562bc3ba6c02150cb8d734f573e746b3837042`  
		Last Modified: Tue, 09 Dec 2025 01:32:49 GMT  
		Size: 68.5 MB (68490610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a6c548c3a36276db37df5e382076ddcff7d94e4b5f7547c404800854a8c577`  
		Last Modified: Tue, 09 Dec 2025 01:32:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0240a1083a9c50bad83e8427187014e87aac09b7fb2fe31ec26e87468e832ecd`  
		Last Modified: Tue, 09 Dec 2025 01:32:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f5d571f256b5f946fee3c157f3ee8033dfcb60763132cfb542ab68cb1117bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41211754a727ef771bbb5be8204e4f52eb7614f4685bba56fa204bc985a3259a`

```dockerfile
```

-	Layers:
	-	`sha256:0f1b511f381b3f650f6a5f196441ec4c4b56602aca3207fc1617e2f3245884c5`  
		Last Modified: Tue, 09 Dec 2025 04:42:40 GMT  
		Size: 5.1 MB (5107813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86b5cda2cffa854a1b2dee5e4eb2310610e8fb5e71b2ff3046e0af780e7f373`  
		Last Modified: Tue, 09 Dec 2025 04:42:41 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
