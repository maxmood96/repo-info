## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6627bfe3f82b4cfe57f72c656c5756f57edc0fcdf08f6eba1dfa547383060829
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2ae7dabc3bda8844ae958901c2e44461b6ceaf457788adb3ea378024cd10ff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a419b6a93a09d204b0df496886597c00d5fa865d4e2957bee7dde1356242a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:34:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:34:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:34:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:34:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:34:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:37:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974478515d7c186335e22d66c2a7dde61bca42ba9c7978f9a54fbf628ade7ca`  
		Last Modified: Tue, 18 Nov 2025 08:02:48 GMT  
		Size: 157.9 MB (157942922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4503b2ddf64ea7f44fb9fb6be5f40b58f2aa317b9388950a6b4b74dae881b02b`  
		Last Modified: Tue, 18 Nov 2025 06:38:40 GMT  
		Size: 75.5 MB (75513333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15be46da2523e4fbe25eb13b78962e4e353d36835cbbd3254679fff4a99d2175`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8778adeb60495f3113e54d5370e9e61dc5cb5686d82dd0c816af7bfe200631f6`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46b89c6908c26c1cb8141377a9f768861f9f1602a51362675e5b68ee611b5b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdd41cfbfcf63ea0b0fa9934eea962f46ae24939070031be7061304b090907`

```dockerfile
```

-	Layers:
	-	`sha256:fb2ff3ea6f073111497425ea8110b37962915c3167e2781b67ce9880ca2611a8`  
		Last Modified: Tue, 18 Nov 2025 07:44:13 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145d12eb66157be1003913f0a499abf5dd4fd30620742600ffbd97d63c7debb9`  
		Last Modified: Tue, 18 Nov 2025 07:44:14 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

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
		Last Modified: Tue, 09 Dec 2025 01:31:22 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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
