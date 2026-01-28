## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:42837f59e926d10054c505af118866e984d07040e29898ab27efa2c4fedd553c
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:05ee02d6f22f3333c1a82231c7e9f6aac39e2e3a7fbabeefefe92e5c6a55f875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189952749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570a22899aaf23d1e80539667ba3aa5b0f322118a69eb9101b0415b752619723`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:06:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6808a7b2c79b683807ccc64102eb6ac5ae8a43a44f939b71e5b06b933a4e7`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 92.0 MB (92045330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c6fcab24449fea807f054e9120ed747983fdf5e860dc7be796bd7f47acfc20`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 69.7 MB (69677805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6dc9a42c656120c2d616b327085f409cb1b37dac9cbe71b880b2e54b264089`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71dd5145156fd3eb1d4a4fe33104ea2f5b3bcc8ff516b0ef3351d0ae915a074`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c90b8600ccc593186e4b030ebacf5dc1e5793587f734e0dbd5799c9f351adfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0575da5f1ae290d179b4b9a145c45dc8012ae61ad55874d757dea480efbbc89a`

```dockerfile
```

-	Layers:
	-	`sha256:2eb256c33f52ff412692007cac3cc0920e382fe5bf727f67aede70db5bdf15d2`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 5.1 MB (5064760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50f8a6502444f076e382827e82177677d45385632e3395af0b627aa2e6ab715`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1caaa5684d7392eba5cd64e917d52639029dd39bf86e9e33293f5245dd797213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6ffd89cbcaa97c118df5932b07784b7a15b4ff8d0aaefaab29d02644237e2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:21 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7bed2ea4dd2853df75e6f7b73ef2b107d4f43de151de10d4241b39f537d0de`  
		Last Modified: Wed, 28 Jan 2026 18:06:57 GMT  
		Size: 91.1 MB (91052493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83b0127458ed6b510380643e40e3554ea2243e6fc15aa3011eebbccdfba9f66`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 69.7 MB (69672731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfd19dbcb87ab387eb3d5439e1eff5cb2297f94fac40cb57d17505aef387b90`  
		Last Modified: Wed, 28 Jan 2026 18:06:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a59298f1efa4008472e90bbbdcbf47898a06c7987a8785a47162f657f75bf`  
		Last Modified: Wed, 28 Jan 2026 18:06:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d91a00d8328709fa396dc77094de5f036111025d7b18fda672f3575a3e7d399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79d1c04f3be2fe48dba4ff473157feed0a8a30459d428dbd9e49e7a9de483b1`

```dockerfile
```

-	Layers:
	-	`sha256:243ec7534a92ad23f4ad07dcb179b14a79addcbfc7c0086d562f2565f401cf10`  
		Last Modified: Wed, 28 Jan 2026 18:06:53 GMT  
		Size: 5.1 MB (5070542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d95cf94bb1d1df28d8ad4cbc12397f22b7790fea41b531184b0b11d0146967c4`  
		Last Modified: Wed, 28 Jan 2026 18:06:53 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:64c207de6398be5f3e2c0f48d8b41e456ba33806402983f3541a5479dee8afd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199194417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb848e8e4e20c776f6a87fcc671bf84b1d343deea8ce6f5dc93c2c31114aab3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:33:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:33:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:33:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:33:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:33:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:33:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:33:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:33:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:33:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e67ec4365d5667a0e97958627f135a74eac3bc30c81b25afca216532ec55e`  
		Last Modified: Wed, 28 Jan 2026 18:34:33 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4f1a5bbbb43fb0e87be14a08923f519b1e4809a3758a5b13693e7ff16b0222`  
		Last Modified: Wed, 28 Jan 2026 18:34:32 GMT  
		Size: 75.5 MB (75513899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cdf1ddbda4c0198fb2be95a44ee4ff3569f0a2452551c135bb236e4160564e`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68f3c55cd35269a833cbb40b657da990bfc7c829e846b2cf9b537ffbfc11def`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15010c3ff1def74c0d5bac9199e16424d875b6daf77b701fe9bf386e5b5bd069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d847de5d2756dee64046cc5b3683e43de1a1765f04656474a3e09394d52451`

```dockerfile
```

-	Layers:
	-	`sha256:04bf7b8ee92ef64fa68ef961787732a0df8c4da3c6ece755baed2238ad8f0bf0`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 5.1 MB (5071228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82527e1d078ef8873182ddd2a18c8104b3163e466f0e749afd0790e4d8c4a711`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bda58cd325b3e7aff30afcc6ceec37c36fd765d7d56de0b7f5674f1c76c7c6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183586514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a8c7d40b4bfa85dc29275dd25d7cd9e4340c961e43d929ced269e91f5cf44b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:13 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:23:13 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:15:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:15:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:15:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:15:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:15:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2259f118386f883a2d8ab34e36f132523e1c60d0a403567de28c3c9dd6d1a5`  
		Last Modified: Thu, 15 Jan 2026 23:23:56 GMT  
		Size: 88.2 MB (88210675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5711f10e12b679c7905127f20d74c883d5955a45b42d265ddc72fe31846dfc`  
		Last Modified: Wed, 28 Jan 2026 18:15:33 GMT  
		Size: 68.5 MB (68490383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20a2d21f80a278a19b359fc90818e7a3ed7496525e215051a9d27012d00b9fa`  
		Last Modified: Wed, 28 Jan 2026 18:15:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f37a492d5e9187889fa4f3981788916fa149d36c897c9a579245415d3d8e39`  
		Last Modified: Wed, 28 Jan 2026 18:15:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9aa33b0250d9b8e0e9dacf4fd9cd713629c72e52933770068e92b05c520a1e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6219d70c6e6be6d8747009897560889bb8e22cf77dc1cd82aa7d41a19dd028`

```dockerfile
```

-	Layers:
	-	`sha256:3c8fa1a6dd66df254be726d2ced725932e1a5a3e26c32802a39edcc0ba9396ca`  
		Last Modified: Wed, 28 Jan 2026 18:15:32 GMT  
		Size: 5.1 MB (5058629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696776217f78c80589633ae6ed60e59912e7a6d7b8bedfe86e94327f7c20976d`  
		Last Modified: Wed, 28 Jan 2026 18:15:32 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
