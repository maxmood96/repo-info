## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:0598fababfc104d02960784c52277d6abdb4201a894e45815f6c8e736e0f56e1
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c65a79ac4573b0e48b7c40395d10c817bc923ac975d35d063afb832a4374d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246467571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feb56dfa28679e5be3c22424ea726171d13016ad84617897bb2ace464b51ffa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de186dc5db30d54fa39ad3ce7c7b448e4ac57f61ffa5c3e7640f82cd1aeeadd4`  
		Last Modified: Wed, 01 Oct 2025 16:10:58 GMT  
		Size: 144.7 MB (144693598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2220c5a0d111d366b7c8087d46a8f7846ba13fb92e633231345e4a3b246faf7`  
		Last Modified: Tue, 30 Sep 2025 00:54:42 GMT  
		Size: 72.0 MB (71995169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8393e7e508df6230a35f28830d93ea036b9eb0768be434770b7b70a44b6b5a8`  
		Last Modified: Tue, 30 Sep 2025 00:54:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881c159a43b6a8294094fd02a83ee84e6238e8da64ab7088109527e2db672617`  
		Last Modified: Tue, 30 Sep 2025 00:54:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1757848a9e335b4356b0b28e466459ce08e54d36b0da4f0e08a5f6c50d167461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb4e5053a4a3851f244d05c5ffa8cd9ece9942659ea56533a5cff77bb104dc7`

```dockerfile
```

-	Layers:
	-	`sha256:62f74c33a91c4025835f6980ed40ccc6f4164f21aab831170cfd94731e4f6b08`  
		Last Modified: Wed, 01 Oct 2025 15:39:21 GMT  
		Size: 5.3 MB (5256113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5dc8fd8b37faa4c61af25b3752ad8064b5c710bc92735845e74c792f7a9be31`  
		Last Modified: Wed, 01 Oct 2025 15:39:22 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f44aa378e4df2c18ccffe0484e0c23400133f4d86bffcda32f7d9bf6a38c060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245488232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38ce61c4f55faddea54dbd89d135424928bcdde7ce5a9a069b3e734d387a513`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff9dbe67f8fb7f16bbd118a69ee0ef99bba88d6a84c7baa5b40aff7fb45640`  
		Last Modified: Sat, 27 Sep 2025 01:55:09 GMT  
		Size: 143.5 MB (143542130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dd38200f4be020a6db8692ef588ffb248969b19b200fbb30317899302bd95a`  
		Last Modified: Fri, 26 Sep 2025 17:55:22 GMT  
		Size: 71.8 MB (71808428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbed1459abeceee1ef82d363406c819a45b2f1acfb80e5c382a1254f7bd7227e`  
		Last Modified: Fri, 26 Sep 2025 17:55:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e4be1d58b3da30e0bcad08431848efd019501a0a859d629409f352de2feeb5`  
		Last Modified: Fri, 26 Sep 2025 17:55:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd9d91de1e753488bcf6a60426304e9c8685877cde65c9cb9b75d876643f0121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27f30ce9e192cfd96aebcc77fd4546643b6048f36825ab7f3962181f76b4fb3`

```dockerfile
```

-	Layers:
	-	`sha256:d41bef0df71d4e3a2b56d45069adf6afbe965db7df25297df419cc7768911b6e`  
		Last Modified: Fri, 26 Sep 2025 18:40:24 GMT  
		Size: 5.3 MB (5261882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b03e3c2da1a640e53c783846d95fe7b16db3854249b0e2382040982820cd35`  
		Last Modified: Fri, 26 Sep 2025 18:40:25 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b9692d02a42835c3cd0a9686ee3849015145bd14b6ac5dde005a632282f0e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61081ccbe3a20c90d7b60b9d3451b0c0e95ab9e599c99ce6811f29559ba3a834`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad50b32027f930ce266ed2ffa46f693b6d78881a7487f10923edb7f90a09b42e`  
		Last Modified: Sat, 27 Sep 2025 20:14:17 GMT  
		Size: 144.4 MB (144372861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea378ae8b89d3e2b12056a271f15c1ed257c2d0d5ed9726374ba3938fe832fc`  
		Last Modified: Fri, 26 Sep 2025 18:21:19 GMT  
		Size: 77.4 MB (77395697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2c5739cf993d197041838efa9ecd2ab8c6f3db64faaba3dc3d2d3bea98e2f`  
		Last Modified: Fri, 26 Sep 2025 18:21:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fe6b086b62a29d0392e7075d0eeb4412a3ecde13023232bb9881404489bd4c`  
		Last Modified: Fri, 26 Sep 2025 18:21:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3cf2edfad8615d68b78bbfbca10e250b23ef2d1ca952fb7100f725cdd8af596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c137b4b3bc014342553dc51763869b3b4f1a74e584bdbf7b7963bd9101d9695`

```dockerfile
```

-	Layers:
	-	`sha256:16a0cfbfdea4f7b51b311a09d7e0da23bda3c73dbd8273830c738b5fa2415460`  
		Last Modified: Fri, 26 Sep 2025 21:38:21 GMT  
		Size: 5.3 MB (5260484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1c60770de9cef34330a5ef0ab2881ba0c065378d5d0fd30e9f58df4a22e1e2`  
		Last Modified: Fri, 26 Sep 2025 21:38:22 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:380a56734bb2a72b0a329219f31de39624e1c3a26e90cde7a5662d8ce2f1773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237729064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8d2278a1edf667b7d848a12fefbb76bced23ff744fb1b7202bada934084f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc8e49d754731aa48ab39d3d21f4caaf1eff5c341d81733e409ecbcb6bdb70b`  
		Last Modified: Thu, 18 Sep 2025 19:52:28 GMT  
		Size: 138.6 MB (138575627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58777e8a08128ec2e7cac30c5256ee2fdc7077ac20038e980a3b3b7b5bd4bee6`  
		Last Modified: Sat, 27 Sep 2025 00:18:06 GMT  
		Size: 70.9 MB (70881022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa26b61ebeb7fa3e69e48190996a8ad3ea63393412b0bd78e503c61a315ffcb4`  
		Last Modified: Sat, 27 Sep 2025 00:17:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8c39cbf2dcda6728246472c73754a13252a4d2011d28307dcbbe9c63de866b`  
		Last Modified: Sat, 27 Sep 2025 00:17:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e40294efa5d0fc09928a63c85a00f55dfaae2ea1a48d3bbcd1f2728b31e3569e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d805b67eb46dc266edcd1f7a9e8591db29907fac9ce370b63e9e5c1c31a20cd`

```dockerfile
```

-	Layers:
	-	`sha256:899464412dda06dde887ec22f8b15245e86748c89aad8cafb48185b5f4b31cbb`  
		Last Modified: Sat, 27 Sep 2025 03:35:51 GMT  
		Size: 5.2 MB (5243658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489f96b4cb958d41d68078a2c07478fbed07fb1612cb35a1662890dc5cd7950b`  
		Last Modified: Sat, 27 Sep 2025 03:35:52 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d545b55de4fc6bdeeb7e1468e7e3045f3716ef98935a38c297b8b1be2a583c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237516195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b149f941b879c61e9097a78a69740420baaf411e5861871675cb24a6928864`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070d385935fbd564818a7d81bf8c54f6e21bfa32a817e475cffb8ec32a09b4b2`  
		Last Modified: Wed, 01 Oct 2025 00:13:00 GMT  
		Size: 134.7 MB (134724338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29be377a82ef9c5800ebe3b5dfde56a596d600a95dbf091c3a0353d1b1edf04e`  
		Last Modified: Tue, 30 Sep 2025 13:28:23 GMT  
		Size: 73.0 MB (72953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c82fe3ae25230aa4a62a60bcd44f0cb5a8b3fd5d646b46a3f846a67ecae52d`  
		Last Modified: Tue, 30 Sep 2025 13:28:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234882f22641844631b6b7fb0aa9bf814ecddc8635d93fc7197ed4617c6689e8`  
		Last Modified: Tue, 30 Sep 2025 13:28:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ee4c98a80a21898b3fb9824caee9cc8753c0708519d6b5d38309815a26fe6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8368aa519da41a59af38a2349381b95092453a7219fbb452236531045d12cc8`

```dockerfile
```

-	Layers:
	-	`sha256:2bcc0d808a281388f9295e9c9312bc5e15f28c9ba132423889b5618311cd0e23`  
		Last Modified: Wed, 01 Oct 2025 00:35:41 GMT  
		Size: 5.3 MB (5252037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73eaa53417158ff7cc058191bef833007157d9c92d86402778f931524a8f9148`  
		Last Modified: Wed, 01 Oct 2025 00:35:42 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
