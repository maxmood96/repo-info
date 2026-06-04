## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:01860a34e7edc90bf246b7c35d233b0573b0c4c0bcf2e4b11e362ea0d73b972b
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:793a21162411853e05bfbaf71ff3b193f84107adec62dd78a8f1330845437bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277734728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc006b348fd7a42e9e9c9b367ef0117c77e48bc113d10745626931592551c9f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:09 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:09 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d49edf5c9ed9af8350c097ad244adfbc2f03a33341c80b80ec4b8de3fc1645`  
		Last Modified: Thu, 04 Jun 2026 17:46:51 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37cc0bc5b2255b1083f9a1e6155931dd4f62a7ab62d7995aa5cd16162ad374c`  
		Last Modified: Thu, 04 Jun 2026 17:46:50 GMT  
		Size: 82.5 MB (82517608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d582ddc9ff08ab15c4692f711f8aef09b3c3bc7551286b6e4694fc3c8d51f2`  
		Last Modified: Thu, 04 Jun 2026 17:46:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0762c85f439a43f56161b6991a7097462abfb00e2a8790bcb47171acdf85338`  
		Last Modified: Thu, 04 Jun 2026 17:46:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1862c135503cf1baeaf271cf4b08d4aec1de9c8766d37f908f09720be359b2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb66b1a8170814eb1fb92231922e464f025a1352bb19249c31b00196fd23f61`

```dockerfile
```

-	Layers:
	-	`sha256:89b7dfa7d14034d2a930932dbea56992550883af8ceddcea938147e3d16b4859`  
		Last Modified: Thu, 04 Jun 2026 17:46:47 GMT  
		Size: 7.5 MB (7468771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6979428bc7d46cebeede205b43fd7e7185552729f2d23e0041b7f1845297b629`  
		Last Modified: Thu, 04 Jun 2026 17:46:47 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e4bf418a0f7d4afb168268dfb8a3d4fc379a6d8fc6a30375aea2565c35283032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276736163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb09840945a7d40e93017f24519bac1ca86aa87c03171896e10e0cbbd088134`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81b6fa02450db45b86a4c221f3f2c217ce7097acf736364d60fdba0e42069d2`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48602d9026a1a74200889709f812036d11b5c5609fe9be09ee1d9eee3e2f2a2`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 82.3 MB (82338540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0801f3f89045219dec85bea2c1ecf33e84ba525130172d4a2996a4155405f0f`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17af942803bf3c752bb32220c533c9a3bcecbda272759277dceb41cabceb0d8c`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f0278e2da3512cabb4c48c3cbfb18f136aab85c69e62e8cf417d02debec8daa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30422ba78f1d04ca56df08872809846b1ba02be669ba608aea942012ba9667`

```dockerfile
```

-	Layers:
	-	`sha256:93c189be7b5468592a6cf52d86e26c2b3ef856537aab45db51c0d03b558bb5e7`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 7.5 MB (7475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea51dff225d2f34d3955e1e50215a58b7f065046c6a451e775e62c8c23e4e1b`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 16.0 KB (16025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f85f7feee0716759d34c4d5761893004b3318f8e053b45637e76ad2b8ee6dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286837281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177265d54ad4997a34db50b65401e07cd6398b7235c333cde2596e3126047c0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:56:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:56:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:56:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:56:04 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:57:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:57:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b56959c90c5f0fe14cf07141a8ccbb5fba2b1e9b43bac05ab20bc6c254eda`  
		Last Modified: Thu, 04 Jun 2026 17:57:46 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ebb907f06aacca3fd75882735b8ecd5cb02a297fa4ae79c61549ef21448bf`  
		Last Modified: Thu, 04 Jun 2026 17:57:47 GMT  
		Size: 87.9 MB (87937944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439bbc873207caa070ef845e8e407f52fb17ca10c30fea691427417c15625631`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bbb08d21dd966fd6d86549437031ed6ed2a92bf68fe01aaf2e782931823ef0`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:52da1908f5cfcafd0df49b6fc126039e454dc1906a07520fbbb39e690df8e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaa31a917e61511cd1a61efbaf3331d83a8934e024bd68abd9e6f8cf5e4488f`

```dockerfile
```

-	Layers:
	-	`sha256:5dcb4903615f5d49b98472525e698c9422728d5a931c876f46451cf880216e1b`  
		Last Modified: Thu, 04 Jun 2026 17:57:44 GMT  
		Size: 7.5 MB (7473192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c80e0d00023918519eb0a12bd1b9d890f1479548241b9ba7417e54abb6bbf85`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:6114aa3a2ccfabbb31b9679567a58e546ff7f7322d920adbc8e3628f25937575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268792848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262cc62154d74517a80099f5d1d0175afaaf454cfb956e575412c3759bb973e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:51 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:43:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:43:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997d64b4d0625da41bfeda266648bfdd25de100e2451263936ceeb62cb02887`  
		Last Modified: Thu, 04 Jun 2026 17:43:41 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4555f2ac6fe19dd73f4f64528ec01176e3294a904586163f771fd68d8c2b643`  
		Last Modified: Thu, 04 Jun 2026 17:43:40 GMT  
		Size: 83.5 MB (83501619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9c346f3db9600164fdb42a58cefe91581cb352faaba4add4569bde36030a6e`  
		Last Modified: Thu, 04 Jun 2026 17:43:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26779257f3d3299d9cb47e3611c718b164bbccdf05b46ca2bccd115c6f6bbe50`  
		Last Modified: Thu, 04 Jun 2026 17:43:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d8f8f5d693286690f6a547321d2e1ca04565168f9f34b606e18e9f38f5d6061c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3138e514290d5f31516965df5b2889e07f720efcf01d4e96355dbcf5212c4e9`

```dockerfile
```

-	Layers:
	-	`sha256:a2e29351cd9ed8df9734b752dfb7cd27b1c7a692925b8a1dbb74586983d11c9f`  
		Last Modified: Thu, 04 Jun 2026 17:43:38 GMT  
		Size: 7.5 MB (7464693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760f818d62e91b811ab558dd36440901c8a1c09edefd3fa1b0de3d0ca16303ec`  
		Last Modified: Thu, 04 Jun 2026 17:43:37 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
