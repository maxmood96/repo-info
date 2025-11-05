## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c59496f5ebee7e5ab187fd7bb6caa98a43e026ea7a0d8afb1286034fca6b741b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e34a2f3da8c9a41d63fa6ba7c2b36bd747fb0cf2bfe79d1268e432a9c769729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246467703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e8e6716535e5919134d158761f229fcc6e49614c56cb2eeeda9593779c0008`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:30:52 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d900fb75486e7bedc9eba22175a21164895ee835e3bda20a91a83989edb74c5c`  
		Last Modified: Wed, 05 Nov 2025 13:20:04 GMT  
		Size: 144.7 MB (144693318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bfe50bc20774dc47c7dccf41f177f748a9d2d7cf5294fa15d294e1c200b242`  
		Last Modified: Tue, 04 Nov 2025 04:31:35 GMT  
		Size: 72.0 MB (71995241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925ffa6d32ea289454176d7ebf5615dace937a53a02f2a8d4a565af3fa4faabb`  
		Last Modified: Tue, 04 Nov 2025 04:31:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30a699e3005e54cfd5a66794c3783f844646316e7d1cefd6270e61b9a99400a`  
		Last Modified: Tue, 04 Nov 2025 04:31:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c12de48c87cb11f583e68ccb599edff6ba884cb4f08cbc6e6c2df20a1c964f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906a871a0952647d9fe5f83e21630b400baa831fa07f75dae3742ab46ba8d830`

```dockerfile
```

-	Layers:
	-	`sha256:000b461ba56d66a006aec4d647cb50bc246e982c8df2debc9da9ce91a638f119`  
		Last Modified: Tue, 04 Nov 2025 10:41:31 GMT  
		Size: 5.3 MB (5256167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35da23280250cc89db9082c9af71960c9a94ac20fe4f4d1cb26d7320d8907355`  
		Last Modified: Tue, 04 Nov 2025 10:41:32 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d5920f7f1adea552551212a06aa59e8b65ee25df810495f4cf7eb7621b55143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245493947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34f720fb3f8275e519efe7dc7f263014ce72c41bfb851f939e021edee01a329`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:44:41 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:44:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:44:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:44:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:44:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b109521e461a35ea39527f27ce80da17e13a56cda5aee30dac56745aa91fd6a3`  
		Last Modified: Tue, 04 Nov 2025 22:42:08 GMT  
		Size: 143.5 MB (143542163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66030cedeea13eb96fa53f6f83ef2c86a10c9353824b02d168af7116967af60e`  
		Last Modified: Tue, 04 Nov 2025 01:45:38 GMT  
		Size: 71.8 MB (71808451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7c308e6d65dce6cdef66003dc09b12dbc69527ee1dc6b3cc2faed57a12b13d`  
		Last Modified: Tue, 04 Nov 2025 01:45:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824f9a0c5cbc405131be9930bbee03518a4a263cdbb42b144721ab8e8ccc7e5`  
		Last Modified: Tue, 04 Nov 2025 01:45:28 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6662511ff273d7edae8b24d41c7fcde842a2393deaa3cba0ac658850738de007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05f0b782a0cd63d1df025b485888cd0a395f8966aec9338785770d990ee2dfd`

```dockerfile
```

-	Layers:
	-	`sha256:f34c5230800aaaae6b7a5568a93ecb602d1a87d2416c99b78d6efc2a0f78ff2e`  
		Last Modified: Tue, 04 Nov 2025 10:41:37 GMT  
		Size: 5.3 MB (5261936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20e062283a8f7bb3564c3570c67ba9fe70cc9cf6f1aaf13d4050a8d5764afb0`  
		Last Modified: Tue, 04 Nov 2025 10:41:38 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5f33d9bbf8977a41d736ed7cbe9f4943226124b1d6452ff461896fdfbb781990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255368850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbb57ee57b1218c98c5aa1a57e62a24eff780951c029c83ea4262fcb8a023a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:26:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:26:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:26:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:26:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:26:38 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:32:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:32:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:32:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:32:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:32:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b0ab8b1677835c8663961f0f2a2f46d80a48ba192376f309d53c55e8a5e398`  
		Last Modified: Tue, 04 Nov 2025 13:28:04 GMT  
		Size: 144.4 MB (144372909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855cee9a4d5d5d9b1c3db7bfe607b3218bbf613f177446608906d11df234f1e1`  
		Last Modified: Tue, 04 Nov 2025 13:33:30 GMT  
		Size: 77.4 MB (77396252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cae65e3ccbc1da2de1c3ab5d6d6ab75db734965bfb9de3855d6de7f33831cc`  
		Last Modified: Tue, 04 Nov 2025 13:33:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfefa3ef8453ac919d22b5383bb7a23cd31e15ba835ff11bd98e32325ee1a96`  
		Last Modified: Tue, 04 Nov 2025 13:33:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:139b061bb94aa515935a7c83617e2de92ceb80bbd4ab585477924d51a7c4c4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be012df9b326dca3e1218c53e219418d572f9c77e4a655317a47854d224be43`

```dockerfile
```

-	Layers:
	-	`sha256:5995d1e3890ee5d9184c3e929d62d7bd0ba64487888eb21236d8fd066c7ac05a`  
		Last Modified: Tue, 04 Nov 2025 16:37:37 GMT  
		Size: 5.3 MB (5260538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518341b48a7877a08178d0dc211a59a9185ea096db7277655c84cfccc709eff5`  
		Last Modified: Tue, 04 Nov 2025 16:37:37 GMT  
		Size: 15.1 KB (15058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bc4f644f800dd594c14788f623ce9fbc9dee0744601c98c4dbb761f99c86f6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237733146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10df0cdbb2da039cf7dcca82f5aad018dea2b6d5e579b9c12143858e3f7624cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de474e3dd67de6ede0e921395a3668a1af187dcfd0cd62fe28f9cc74e299d6fb`  
		Last Modified: Fri, 24 Oct 2025 01:09:36 GMT  
		Size: 138.6 MB (138575664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16c1db97e0d9c3a35ae3058dc5aa6bf66b6c9a7bf1e92724831f8deaa50add`  
		Last Modified: Fri, 24 Oct 2025 01:49:35 GMT  
		Size: 70.9 MB (70880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848be88cfa88dc4b9c4bfa622ac56f296571d333d95dd42d0fc49eef2fedc1aa`  
		Last Modified: Fri, 24 Oct 2025 01:49:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eb20d9250c9d4e704356ffc7ac415ffcac5f16fb8638234668d8a6003e64b6`  
		Last Modified: Fri, 24 Oct 2025 01:49:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:206cb76932e2e0636c1fe423609e8dfe34b71482790b6bd7bc201a126bede74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335df4d5027854b74e8837bbc5ca593e0fb2d2b755ea8e8101e7e0f71f56b490`

```dockerfile
```

-	Layers:
	-	`sha256:bd0c0570521ca94e2eacb8cd09cb11359399a4a8f6ccbcba3d5225cd12324e51`  
		Last Modified: Fri, 24 Oct 2025 03:35:50 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021adfff7ac7dbae96bf01569b2f0f97694b9dce45052692111454acdcfb1838`  
		Last Modified: Fri, 24 Oct 2025 03:35:51 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a466a4bffbcfe2dbb3c3e2093ab98b2570b6fd6fd7d10f224aad684165fad5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237515610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f3bd107de8eadfe9ee1788ea79123acbc9d4f0509a4f8d9c04aa68fb6841ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:00:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:00:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:00:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:00:58 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:03:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:03:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:03:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:03:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:03:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef97739b133858c91a593c8e478df23d1f122cef3e6432d7b402f82caaea1d`  
		Last Modified: Tue, 04 Nov 2025 13:01:38 GMT  
		Size: 134.7 MB (134723609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672638d25513c5549f47dfff0e7c84710d5960fb2ce0b1b3420780d69f17cf30`  
		Last Modified: Tue, 04 Nov 2025 13:04:05 GMT  
		Size: 73.0 MB (72953570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abdc278831c8cf33892892f3e3789060a5416fba1468be19738568784bc67d8`  
		Last Modified: Tue, 04 Nov 2025 13:03:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75efccda0d5b1ae771a0435a71907bbff029970f2c01067c7ccedd8172ecaf24`  
		Last Modified: Tue, 04 Nov 2025 13:03:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c9802a82aa5fb94749ead9f96e833f81659bef116b6f758406bf4491d91d7301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e19acd71f0bb411957245d3d7067a533ee67ab2abb8d17c31e4ec50e1a4f226`

```dockerfile
```

-	Layers:
	-	`sha256:50d268a7badfa7d4d9e86b0f31150f0a0857a0fda392023f5c1a8f66f4fe10d2`  
		Last Modified: Tue, 04 Nov 2025 13:36:41 GMT  
		Size: 5.3 MB (5252091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6542ce83c7bd294e98fec365ee3098b5fde066f4caf83de8a4883b8cc6f997f`  
		Last Modified: Tue, 04 Nov 2025 13:36:42 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json
