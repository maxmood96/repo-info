## `clojure:tools-deps-1.12.4.1607`

```console
$ docker pull clojure@sha256:360962d6726d78750916500096aa696c63ac7b3594790419e43c191ed3168129
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

### `clojure:tools-deps-1.12.4.1607` - linux; amd64

```console
$ docker pull clojure@sha256:c45eea841a8880b85e9ae01b568716948e1480e3f87df0c49bcfbf5d4b9a7ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221907651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123ca63b938cb857586e1819523b3a3e09425b7f954edae843a3d974721f552`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:48:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:16 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:16 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d220f1eae83cbc5e6517425e0b4ed098349075b01599d3ddca5f22065011e1f`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c80eca64902ec22f98e192bc3ee445ec0f7fb2c8247579e22297bfe471cf3e`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 81.2 MB (81161517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30538e33df321c7fe93e34a0ed9da2aa6a581983941725debaeeb9593c52ea92`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47f198463d4c4f0bef4c06409848e9d8cf7ef6088c61916bc691d17128daf13`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607` - unknown; unknown

```console
$ docker pull clojure@sha256:a88e835070dec56df5218d0652e0d3cf1a59d60f90600df86cac6236fea7a173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e83ead82a4141b1e69403240b6add592e7b7992efc5b47ee5b6eb81718f698`

```dockerfile
```

-	Layers:
	-	`sha256:21cd9393661c9fbb1c5dc194ceacb9095435ce6f50f5fbd556f72228c9572e73`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4560c4af94e17d47cd2625275ac75fe6d8c8ebee0e34fd10411dc856838318c0`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c67278d96d78b0869cb392d4549c4fd25f140e12941e816a2c2469f4aa4c197e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220817481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566fb30acf23923609979392b588252bada196917fd61e76176eaa95bb810f6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:48:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:17 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:17 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed32f54341c5f6e91646992c4ed8171f1a2939a5fa039ead15e7bcd75455c0f`  
		Last Modified: Mon, 02 Mar 2026 19:48:50 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c6ade6b317b73e0d5de90d40f5361f8b7c38c1baf18cb5c2805c745822d07`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 81.2 MB (81154923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b898b2728f52227ee8f14658bb846d02a051b959bfc0beaa524ef3dbbdb973`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b00a3e30718e1be5e159b3d70a61cc4338aeeea0d3982e3ce38818a180e0`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607` - unknown; unknown

```console
$ docker pull clojure@sha256:2a9ae3e769612e875fab7bbc6b050ee1bcc18588ef16658926d87d1c88d9543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb150aece29cb2c19dc1ea2d5eba4c7f33d0f15934d4cea06da790ff398f1c63`

```dockerfile
```

-	Layers:
	-	`sha256:22764b39ab8f938fd8198381860ca2df3386be7d61761dd27f952aa3a6e5df75`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d95e90386310f69b08b8d689935d7d00b0373f0be258742c4c49c8412d21e43`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607` - linux; ppc64le

```console
$ docker pull clojure@sha256:2ebf0d81dd707acdf19179a4103c02e56102cee367c06296741d44623405a021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230974489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de19979b89a011debb4d884ee5c7ef25642b20ea33618acac9d577316145bc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:33 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:43:34 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:08:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:08:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:08:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:08:37 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:08:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144f17a3e7d82510fe9dc0d0bcec634fee1e230b910b421966d0efc2cada5dc0`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 91.6 MB (91632868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb4136300a3a352bb092b9be7f1892a097b94f1203734897c52d6078f16d2e1`  
		Last Modified: Mon, 02 Mar 2026 20:09:15 GMT  
		Size: 87.0 MB (87003783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931fc89c683c14795b4057e6af61fcd82e0ad9dd89a60d88148b59f1426baac8`  
		Last Modified: Mon, 02 Mar 2026 20:09:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4db5322bbea29a9f77b7630772c8df44b97cc65fae9f0f8d8d5453a10db969`  
		Last Modified: Mon, 02 Mar 2026 20:09:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607` - unknown; unknown

```console
$ docker pull clojure@sha256:e0896e5302a814e0c0be44f281e06be2b84811c8d72ac3e0639c99b461796478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548b82c495631e19096e76ad1c5e62d7a4024d882fafeceadbe236aa30b229eb`

```dockerfile
```

-	Layers:
	-	`sha256:53dec1bc524d9d227a8afb0f393cfe8dd9325b20d7c1762286c48f12827eaf40`  
		Last Modified: Mon, 02 Mar 2026 20:09:13 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbe01062d9a2836b3413a10f3daa1946ac5c3b07b5b21fc26d54757154b05ff`  
		Last Modified: Mon, 02 Mar 2026 20:09:13 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607` - linux; s390x

```console
$ docker pull clojure@sha256:8423c0eb921c8c76dea32ff3c4b94b8d93c3ba5b864beb4bbbdf57cbbb99d77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215357628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98e7d3953cdde7cf8238f6f40bfaf82dafbdc67893e4d527722bd4a14ed1bd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:21 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:21 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a71e85f0db1433ac034081f947b0fb90b20a4b6eb84e397b7fbc60abbf0301`  
		Last Modified: Mon, 02 Mar 2026 19:49:09 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6e11225508d298e01cf106ca8d72a884d959454d12670bfd8c439857894e5`  
		Last Modified: Mon, 02 Mar 2026 19:49:09 GMT  
		Size: 80.0 MB (79974674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bf83b89d201e024fba97f7890bad43d1ce690a02ab729171d3da922cff1231`  
		Last Modified: Mon, 02 Mar 2026 19:49:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7216a5cfc8331ed032d7f43dd06c1f1b98a3c97845eae2d199411389cfe4ded5`  
		Last Modified: Mon, 02 Mar 2026 19:49:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607` - unknown; unknown

```console
$ docker pull clojure@sha256:8ee18b644e7e002db67e3d1a9ae5d9a05b39cab6f7fef5a3bc011b32e7d4f9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2e5835687b310b9b6c1091562adfbe8b20f9ac852a3903452c456815b472d`

```dockerfile
```

-	Layers:
	-	`sha256:5ca37d27276ce7666dee0c9930875fce8d9939b02f3812b333df59c8a36c13dd`  
		Last Modified: Mon, 02 Mar 2026 19:49:06 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1d3c3b69eb9b600739a7a93531e36dd16569efa8cfeaf7aa4bed02cb42acff`  
		Last Modified: Mon, 02 Mar 2026 19:49:05 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
