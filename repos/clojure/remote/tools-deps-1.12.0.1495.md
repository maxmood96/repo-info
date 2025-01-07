## `clojure:tools-deps-1.12.0.1495`

```console
$ docker pull clojure@sha256:4141b44ed6d470f89fea85b3ac5e2953d5d427f6c8a646f12a044e77acfd9ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1495` - linux; amd64

```console
$ docker pull clojure@sha256:a26ddfb43988eeaec6e84d6feb657daba0d4dfb653c5eff0c25b6b0489ad4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286842665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f5a205685dae92912b6f74e001fad8b706302d3e08ef926e567c3d6d5dd1b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c180ed4e2362b6647746ac5d015b6016cc78c4ebe2c7432970b8606edb9f16f1`  
		Size: 157.6 MB (157568719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031e0914cc609c5f0b946f9693c4d23394fbd1b824c39ecf2e17ff511be3181`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 80.8 MB (80775844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37186805489dd8d0a22649337546e4ba97cf174721290a3b02903a0df2879e9`  
		Last Modified: Tue, 07 Jan 2025 02:29:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4884171d3d96c9d18d185e8fcc225e1b7b15f620c6178f15d4f1ab0925070ae5`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495` - unknown; unknown

```console
$ docker pull clojure@sha256:7f12812fbef664f306eabe82b244bb87ca1115e0b72d4e7600059de086521c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd146f2d2050ca4956a2d08a7d536cd18ac866f8d131e40e740c8efbb944fd0f`

```dockerfile
```

-	Layers:
	-	`sha256:59efafbb791611d9820ae4bb6f6edaa0d40666adbd442dd9be64b8b3a3a217ba`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 7.2 MB (7176182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d1fb24d34505267c55de6bab7e4414691951b17243ed87658704e9ca013abb`  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
