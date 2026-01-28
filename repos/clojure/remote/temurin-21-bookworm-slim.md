## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:8cbb8d16351a2d4a24630ae2d1e4901b30758c39324480e18511751118e49068
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
$ docker pull clojure@sha256:032b2f7b673c4401b25937ca5f701e28786c5a61e9040f848fca633e79a59562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255733663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643986dc9cbb8ce0d932e6f5d3130e5f5775f5aa3c1dbaab46197228a23401c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:05:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:38 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b4570ad99ee8849cb912a86a37c893c39187a1c25b8dee1d94731fdc3db16`  
		Last Modified: Wed, 28 Jan 2026 18:06:13 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5586831d81c324a50ab18aec1a5459a9d4eecb6900fdfff60e1661bbebaf170`  
		Last Modified: Wed, 28 Jan 2026 18:06:12 GMT  
		Size: 69.7 MB (69677994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8169a1300edf48291bc3dadaa4803f53fabbcf50bc475871db538e35da1054c8`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d45052f9e085f62f97807fb64c481b21bd8b9175d24b04975f9bf0e6f0eb2b`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31a721ed81c047b031426c1b1262b43cb954f6b391fc5a7f4d24fb1e0adb092b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec56203f40535fdfd2677a51bd3af87095e0e752c513b753942f4f35cd52b90`

```dockerfile
```

-	Layers:
	-	`sha256:a1057a8f6910cf6b0a30f932953b2d930be2e19e057a337d8d298c80a7b175a7`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 5.1 MB (5116504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f568a138adff823b0b3ec90a72cd14190c482261f127acc916db35fe89ca2c`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:249239d28ade2a1871f59b61d0d8e77009adaa117ec8a45db4946c9d4488dcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253889332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef2820af717dd5e975ec06be71594ceec049d93437893d399c7796047754110`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:05:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:17 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160765f1970519a0e62c40d8e0a715dcb590fa304eaf952c7aa96f092877b5b2`  
		Last Modified: Wed, 28 Jan 2026 18:05:56 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75ff0494c21bc2a98dbf6e36d12cadac3f717346980096f8bfee27fa8b438cb`  
		Last Modified: Wed, 28 Jan 2026 18:05:54 GMT  
		Size: 69.7 MB (69672824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159d8a6e6de52915456a45343e8d9bd2ea5cfeb06daa4a389884fe1e05f9fba`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583974c7868ae87967cebc96d648ad372ac0a3c8fdbb04a1f534e7160ca98850`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e8666daf901a7c1240b27ba9427f0d43637e4baad966322355bf44f913eb972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8ac320b141d521eb86b3e18a5a03194ff544b18213cb750274f2a15741b099`

```dockerfile
```

-	Layers:
	-	`sha256:da68e8302d29a29f1344dc7931a4bedc44b8656d2338f3143d0bea395df2781a`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 5.1 MB (5122265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a520d9f3911b895317a16c9119584f90ff057b6c091604392ba3a73d5b53eb5b`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:24a720ddbaf45942a3b1becd1d0359811c429b6e649a150afdfcc42e67f71c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50edf740a919ba955cc7f7c6021514cec07fa5b840789c439bb770dfcf571a01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:27:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:27:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:27:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:27:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:27:54 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:28:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:28:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:28:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:28:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:28:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4beb8420a420e886202d4bb4012c364c66217c71a8e39a661ce8a895a851c67f`  
		Last Modified: Wed, 28 Jan 2026 18:29:18 GMT  
		Size: 157.9 MB (157942968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de31b285f45f67a646d1b28bcac2271528c6b77154e42b45fec71e2f7edc51`  
		Last Modified: Wed, 28 Jan 2026 18:29:16 GMT  
		Size: 75.5 MB (75513908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ad5331d6190f585b21db49e16d01d515535e1bfb838499dc837ddcce50d21`  
		Last Modified: Wed, 28 Jan 2026 18:29:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2773d2c6ba42cbee6cfb36a904e38a58eb952c6ae611657a0bf4ba09e447c16`  
		Last Modified: Wed, 28 Jan 2026 18:29:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c98d1a77b56377f2d78e8575746c5d2e264f69a50af9c9969693798ebbf77fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebf342245b55a14cab06e7e1455e704da5e266b6f765df809f061535a3c6cb`

```dockerfile
```

-	Layers:
	-	`sha256:9d924c238146dc74e9fdd2389cf06c08cbb27e680709adc2cb478c9242d28022`  
		Last Modified: Wed, 28 Jan 2026 18:29:13 GMT  
		Size: 5.1 MB (5121662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ccc3db408a19100e2ecd98be813ff835ac7f780855fc187f64feb9419dc6e7d`  
		Last Modified: Wed, 28 Jan 2026 18:29:13 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:94aedb48baa4c2789af651defd8eefca208af64b999e7e71bf39c6c040054d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242445437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72da5d09953b1073fb41838d1616b170b57c847cbd180ab5d76ecd4f46ea5121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:18:27 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:11:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:11:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:11:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:11:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:11:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee49ba92133d874b741829618924bc0c05855d3180b0f68c63b8b6afccf9583`  
		Last Modified: Thu, 15 Jan 2026 23:19:05 GMT  
		Size: 147.1 MB (147069856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19150c330f536ecc373c4c1c8cf43f81543a7f70f8b04a9ae996435c4e5cc2`  
		Last Modified: Wed, 28 Jan 2026 18:12:08 GMT  
		Size: 68.5 MB (68490126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033339fda8304c3675ba589560a1d42469e24a2ed2f45e785fbb05a97a61d0a4`  
		Last Modified: Wed, 28 Jan 2026 18:12:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec985ba12a4df3565f884936a4b78cf859b7642ff031bbd961073b08b93c92e`  
		Last Modified: Wed, 28 Jan 2026 18:12:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fd209e2c589d907556822eb754c2b06dc12ab640fce44f54e0cff44a40d7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894aa26afee98810675ecf601866dca92e4fd39470eb3ce448a2e21e80e5519`

```dockerfile
```

-	Layers:
	-	`sha256:f4fc22165b47d85dd76219bf590f3fc98f4e811f0674e754a600e5a6e49fa769`  
		Last Modified: Wed, 28 Jan 2026 18:12:07 GMT  
		Size: 5.1 MB (5107825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a038ca2bc66535409fcbcf541bf948a0ca7a3effb8c9929ef9bd53a5b392b47`  
		Last Modified: Wed, 28 Jan 2026 18:12:06 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
