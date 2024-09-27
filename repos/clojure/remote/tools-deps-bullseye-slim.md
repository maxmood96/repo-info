## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ef38563ddfaa3cb274876a0d8bcb0b44de1401691a98a65a6878174e11d12093
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6fceab1908c380867955a515e9802918f00e9c444c9f367dd29dc0f75c0e10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b9a28718434c7206d117178b819389dac2d8130340b6ffb03936006e9baf5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7783a99130b7f7b66efdb2a8e5f8485b540da3e97610dea8db5f5b074c3f0f`  
		Last Modified: Fri, 27 Sep 2024 06:01:21 GMT  
		Size: 158.6 MB (158579256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e00f4a8c34f4e26ac79cbed9a82988bf815e158c4a67edb26b518c82684b1b`  
		Last Modified: Fri, 27 Sep 2024 06:01:24 GMT  
		Size: 58.9 MB (58940240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4045481820e964f53d568c02f02060e6652283657e2683b62844cd754e329e`  
		Last Modified: Fri, 27 Sep 2024 06:01:19 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88315c82f0c43f8f1feedc48b99ee6e50a3c8dfb03b5c878eb29d773cd293ab4`  
		Last Modified: Fri, 27 Sep 2024 06:01:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ae729b4d467ff0e2bad3ff7be460b0341eb942a8af04c8451d15fdacab9a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4828863689dad2f1c999f1ff02055f04c661ac30fd40662df29be13ff02fd056`

```dockerfile
```

-	Layers:
	-	`sha256:776227a97ad115deea9ef5e99d33da2ecc3a00add528d81073069e4e244e9a23`  
		Last Modified: Fri, 27 Sep 2024 06:01:19 GMT  
		Size: 5.1 MB (5103246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd6e0194625806c463e8e0b54f34e8f364f7772677f33b8c962fa0a62ffc166`  
		Last Modified: Fri, 27 Sep 2024 06:01:19 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8960a685a2345912f832947ec306a85ebd40d1f691ede7505c65308d7b51691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245895091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0a74716de263ba978e8513fe4eff961d3795e20f44e8807eb69562d20260bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97724f1be9ac71710bafae377a057c887f8fb27f9e36e7a00f355b8c58ded5b`  
		Last Modified: Fri, 27 Sep 2024 10:42:11 GMT  
		Size: 156.7 MB (156746181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c41a3a7052f03cff12d48731f970270b5f1c6e31f9b44859ab66d2ed66faae0`  
		Last Modified: Fri, 27 Sep 2024 10:45:28 GMT  
		Size: 59.1 MB (59072713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acafea642174d8113f8370d267f490b12d5157e196963bba9a57b04ed9ff6fca`  
		Last Modified: Fri, 27 Sep 2024 10:45:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e1b69c77619847045442c1d707361d05436a535530be8547a9b9fbcd33f02`  
		Last Modified: Fri, 27 Sep 2024 10:45:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23be4fe96798d676cc79c3fec6378a6be0e77f7d13386a33086ec22eb9fec5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618b16bf4924ba5d240842f9581c20da114cbab7ead4780386d16ad875b59981`

```dockerfile
```

-	Layers:
	-	`sha256:451fddf64e36e400285d4d2bc6272d3b8740f4e365e05cbde09a5a6e5d51a04c`  
		Last Modified: Fri, 27 Sep 2024 10:45:27 GMT  
		Size: 5.1 MB (5109007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44df256230a11aef6337031018d40e20c108e82af46826b63067d692fe855e3c`  
		Last Modified: Fri, 27 Sep 2024 10:45:26 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
