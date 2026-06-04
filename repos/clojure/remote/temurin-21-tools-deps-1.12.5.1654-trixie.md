## `clojure:temurin-21-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:4622d7cad86c8d132acd465945997ec8d6a5b12e1c89f92c47763ce7fc408b32
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

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f35d4059528853ef7e5d631952d49de293b6f56da1f736d73c2d79aa2ddc855d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289996037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11038ab5480eb861af0fc51f01c2bcdaf7b76a02a6563648dc5e9d85441872ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:47 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f999de135199965b9b9754c8d91e75993886280bd5f971a5b0e74e6e897acae`  
		Last Modified: Thu, 04 Jun 2026 17:47:27 GMT  
		Size: 158.2 MB (158166942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86813399ef1a8b8e10f7e07966dbcf49892cd36737df795c9f04a192c56886`  
		Last Modified: Thu, 04 Jun 2026 17:47:26 GMT  
		Size: 82.5 MB (82517425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b26890b44fb3d459b62976bacb6d8723b4d2d571795212fd623ef4e45c2203`  
		Last Modified: Thu, 04 Jun 2026 17:47:22 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046665496141d219130cd4642028675ed7cc9f39ed48fee708b18d3241ba5533`  
		Last Modified: Thu, 04 Jun 2026 17:47:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e5110530d48ce9099dccdb363f83e4cbf5445aecdb175aa56d11e8acbadaa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff28622a64698574dac8dbec96427c8f5bd02c75f5a1516045b501b2b0f2f9ca`

```dockerfile
```

-	Layers:
	-	`sha256:dbe341e0a2f39beb94ecf33c3eb8330e55ffeecae96ad95efe2c93bb86cefa70`  
		Last Modified: Thu, 04 Jun 2026 17:47:23 GMT  
		Size: 7.5 MB (7470623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9762c0ff6b4ada0b7bcd7f048ed762ee81c29f706b033962c56e169ecef3a2`  
		Last Modified: Thu, 04 Jun 2026 17:47:22 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74b4856c5d9ee4780d4aeb39bb4f6a60e9fa6702abe716fe090c66a87bdd3ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288472887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752175b45874820e63d34ad5967e95a16e2c53314a294f2342e5568cb1d08a9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:39 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3bcc0dc558cf55d962186afcd7e916ab1bc72e5322cf31bb38cc7e36dafff`  
		Last Modified: Thu, 04 Jun 2026 17:47:24 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d82a44ee26f2d6f06f6823bd69bf5ee8df1f1860353c91261cae37ed921aa4`  
		Last Modified: Thu, 04 Jun 2026 17:47:22 GMT  
		Size: 82.3 MB (82338297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fdf80ae98956035645daab126d62ca3753cd4245d73e6bd56a718a6d296982`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5be8ca8e0e2ade0840752c3540c2a409d7fee9d91d9589bd289e7e8f341a02`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:377e42ea0cd01f1ab1807402fb111a0538216b9a89cd4da5ca541463f22b30f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd484ad81c99ddab652a5d77124bb90ebee765b6d51f3a241698189f0f144a`

```dockerfile
```

-	Layers:
	-	`sha256:cea97bbbd7ce3fcdc27f69f0b6956c136be0395e5471c88427f2cd753e6f96d3`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 7.5 MB (7477016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eea418c7a1330e4903dd56c475f8e4dbac889a56905c75ac92cdb511535db1f`  
		Last Modified: Thu, 04 Jun 2026 17:47:17 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8c7683e0e8ef4e20a2afb7c017b2d8d90cf5bfaea6d31f8f36463b0f51d5406a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299414763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd654ed1dc439ed3b05e8cbffc2231fb261e8f05d5d91203b964b6d5da1aa39a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:02:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:02:29 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:03:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96ab628163acfc4a897a60446de4136b4548cd3582a46ae52f4ea4f52f11fa`  
		Last Modified: Thu, 04 Jun 2026 18:04:09 GMT  
		Size: 158.3 MB (158343238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a1e1cb8580ac4268a3c4e3a37b203da55014fee78fa783d37bd4af826a9571`  
		Last Modified: Thu, 04 Jun 2026 18:04:07 GMT  
		Size: 87.9 MB (87938298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5199c2bae3aab160dd46ffe25d545bd5592f984308090666887c2dcf252f5`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57d62e98e2e672ad6a830b006e5a8298b3d5091337d29685a21f131a31a179`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0fc623ada0ab6cdbdc85c6682ba0b13d55967dca234f9efc43857caffa10d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e845b6d1e3f0c65492d623b065308ac48d16b5b0ccd7bd7f639190479e6910f`

```dockerfile
```

-	Layers:
	-	`sha256:4eddc7a4ced7655c1b79615cff0bd27d8759b575aa0f9bb9f44e9c419b5d9cc5`  
		Last Modified: Thu, 04 Jun 2026 18:04:04 GMT  
		Size: 7.5 MB (7475044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4ee7d8a1c33acbb573665b3bac085f91850e77fbcc51f071bf1262d752aef`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:652f0c35e0ca899d27c657777f1113ee454ef174a762fdbd9f7158f06b6163ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280270973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f27086b3f8026718eee497e07546fa5004df6be0c1e20a6f65236075e7dbdcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:10 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef9aff34d485549e0c0ea2191ed1bf591e038c928612a9abd1c25d328d4092`  
		Last Modified: Thu, 04 Jun 2026 17:46:04 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bed78b7cdb6be1c86488cf1f49866359b67e0bce90f85d6ec54c73f3761998`  
		Last Modified: Thu, 04 Jun 2026 17:46:02 GMT  
		Size: 83.5 MB (83501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60b8bbeefa0c4412be296ad2c189a25d1594fd28ffa92b705f970ae3bfe4843`  
		Last Modified: Thu, 04 Jun 2026 17:45:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5af013f3451f6823bcc46f3c5078226ffdafe4a252c22bcc2420566468af5b`  
		Last Modified: Thu, 04 Jun 2026 17:45:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:160546c84dbef0e7c893838842f0a81c9b1cb5e22ccc5523be651cac1b5aad1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dc10b4f22210d369d3069086ed294f5380ff9b07b22317aff1eef502d1ec8`

```dockerfile
```

-	Layers:
	-	`sha256:877a3fbb483573066f300fd631cbc60c339443d85e1cb79a642228f5827f95df`  
		Last Modified: Thu, 04 Jun 2026 17:46:00 GMT  
		Size: 7.5 MB (7466545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37557e7cb85d41172159f629136e7c0603bada841a1f84fceffb925bb434b7c`  
		Last Modified: Thu, 04 Jun 2026 17:45:59 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
