## `clojure:temurin-21-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:3424a15b260b41c4908826e82cad9ab9beeb089d14f60eaeaf3e389d0d386a06
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

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:e75858eb351b24547f5fa4ae82302837c52db5d311601b3421e346aefa3edf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287433893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5e6ff40ed675ce62318a8952fe938416277ccd8ec5a8132ffcfcaa70ac6736`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b2429c9ab3490373abfeac3c7cdf354f6416c5c46db5b7822c38b135e7e077`  
		Last Modified: Tue, 21 Oct 2025 09:45:25 GMT  
		Size: 157.8 MB (157804764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12217a839e95ee6e744d951f5d5fe9c27f926c3041c824538d2be1c1151f4a35`  
		Last Modified: Tue, 21 Oct 2025 02:23:29 GMT  
		Size: 81.1 MB (81147527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac9fcf051bce0de1957e3df1ef2db03c6de8898b51853f5bf5bd7c56f4e198e`  
		Last Modified: Tue, 21 Oct 2025 02:23:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe43b655354f5cea8e5c7575dbbc39a4c2a35ae999d355a68c13b4458f800a`  
		Last Modified: Tue, 21 Oct 2025 02:23:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:0e025efa8959f3358ddffb39a6db4ca9f5c95327fe5c0a35a822cfe414c2a8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05b98f0f1e08f07697ff59b6382b11866654d7aa310e9b71ef4830fdc59d131`

```dockerfile
```

-	Layers:
	-	`sha256:89144948ef47c90714df161a4923e0dd19a906de38f50156cdb86691e102bc55`  
		Last Modified: Tue, 21 Oct 2025 09:41:03 GMT  
		Size: 7.4 MB (7378676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ad871b46b03af3805cf7e4af08b3bf90e6468bf4cd15df8591f80c28264bbb`  
		Last Modified: Tue, 21 Oct 2025 09:41:04 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cb8908a1f016aacdc76a3fa3eeb441aaf0325dc61fab2bf6937fed2bdff784b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285469859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c4a22f7414eccd732d2a5ee15c4d76be1b092a106ac6e0cfdaae7cfc69699f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d681e9f024d1ea57108fa28ae7b8b16e579ba452864385a8e4dab47a477f2e`  
		Last Modified: Tue, 21 Oct 2025 10:16:09 GMT  
		Size: 156.1 MB (156081275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb37ef235c3a36c93ee57e04cd9c8174e94eb84aa560a0a37708984e6eeb0d94`  
		Last Modified: Tue, 21 Oct 2025 02:28:51 GMT  
		Size: 81.0 MB (81028551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707e7fc91331289d737b832a4a97a39886224c006d2caf540f17773274d33171`  
		Last Modified: Tue, 21 Oct 2025 02:28:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52102409c3f58552b4de008b9b1d3933363db54b7dd92644b571519fe1b517`  
		Last Modified: Tue, 21 Oct 2025 02:28:46 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:fa11ea2d4b705c13bf4feb4595fc95c36850242775548386bae4de4a89f5b501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0380c12e39c62bbe94ee1ba6891c5ab205af87ce7b5558917c8c5ea2685d987`

```dockerfile
```

-	Layers:
	-	`sha256:75ee4b0ceda70773b701aac774fcc56547cb75270d6070a6021630c4f9a0b94d`  
		Last Modified: Tue, 21 Oct 2025 09:41:10 GMT  
		Size: 7.4 MB (7384463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c2c1c37ae249e76591693d428f74fdf86c5924010314db5f70ce904ec941d6`  
		Last Modified: Tue, 21 Oct 2025 09:41:11 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:7608539194c6ff35229a6bc3572867a6530e7d560451ee64b31ea7876d1f7e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297277050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314c4c3cc0fab4dc5d8253f3b7571b1fbbcf9d645f004c8cf9b1edaa6db0bd3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a01cb80034c534616813ad2425335dc4a744989cca0d63abe91b96677336f9`  
		Last Modified: Tue, 21 Oct 2025 21:54:45 GMT  
		Size: 158.0 MB (157963459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379ef16e1ca12e432e45be88cc8c3cdfe4484e5cdf33fff50205b6d2b3e0b43a`  
		Last Modified: Tue, 21 Oct 2025 16:10:42 GMT  
		Size: 87.0 MB (86985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862da8bb019e9704fdf39c19862ef51ec02756a7386d0f0c09f27b47deaedb59`  
		Last Modified: Tue, 21 Oct 2025 16:10:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296a7e16af33435bee7ccf8367eab27dcab44a44cfe9e0a6d0c3e851a78a09b`  
		Last Modified: Tue, 21 Oct 2025 16:10:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:8b0136a447efd7234a8ae552e64bc82512efb3751d0b596105e430d3fb930618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6b150ca280166beaa65ecf86784cc168b161756f1313a6c4d5b4de02ba3a5a`

```dockerfile
```

-	Layers:
	-	`sha256:44693f0ad31e96f6165d994283e21a2c2f0396bad03d7e79467fd37a51f11445`  
		Last Modified: Tue, 21 Oct 2025 18:38:32 GMT  
		Size: 7.4 MB (7383902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253649cd54b560546e90859010cfb333382e277874dd0d23b3868782707625f0`  
		Last Modified: Tue, 21 Oct 2025 18:38:33 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:0ba8f6cdd919e13ec3cd7c3c2436513cb694afa914be36d0f813eaeb550e5696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274122298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e93f7b58b165700daac4c711fdbe30c34eb26b0bc4c099b9b9ce6c27f04b321`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403269c5fd49cc426b8b7a3d4a82468e48977ff3add76fc61fae65c76a438d26`  
		Last Modified: Tue, 21 Oct 2025 22:25:15 GMT  
		Size: 147.0 MB (147026968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510fcdac85025759920d05c8fbc6654a247d9803b3293f4a830e5d73d6ee8c4b`  
		Last Modified: Tue, 21 Oct 2025 22:34:53 GMT  
		Size: 80.0 MB (79956767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a145fe26c8719b763956b4b92ddca617da1c714b63d320834db4ddde13274`  
		Last Modified: Tue, 21 Oct 2025 22:37:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ad74cac77241a958533932c4b388fd987bdbbab1d923afe1ecb74074bbdd45`  
		Last Modified: Tue, 21 Oct 2025 22:37:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:ed5f4929b6be79dd0c6a11ffebdb26e41a57f2d9b09adb9624b5499234eb3877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443a28ef3df56184f6564ac03c48015ed4f06b61284e874cae275a4e5fa7770d`

```dockerfile
```

-	Layers:
	-	`sha256:b536419e94b4b1533a7c40e5eef9feaea1495af8e16f5d908fd2407e407b5230`  
		Last Modified: Wed, 22 Oct 2025 00:38:30 GMT  
		Size: 7.4 MB (7369995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8cd1cb62c5579f9a753bbd02dbd17d056bc73e7046325f9738d00e93f09afee`  
		Last Modified: Wed, 22 Oct 2025 00:38:31 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json
