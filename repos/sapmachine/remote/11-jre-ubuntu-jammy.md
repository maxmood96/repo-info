## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ba9627fe8c8f2008ff325a9ffea160cd207f7aafe866df3c70467c22323a4f2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:01f0229bb979188026f4de3779676f1fe8d72e03838b0bfbaa50c7ef39d151ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79242218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0ece9605906721758d68667c824e8e74b23fb501e2ca5c6bb172bcc9906383`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:26:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6692ec87426e733241756a96cb751317fa8acac33a1c322bd53569db7e91a15`  
		Last Modified: Tue, 17 Mar 2026 02:26:33 GMT  
		Size: 49.7 MB (49703698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:33a42f71d3d4c2a4d729464a8bbda555fc954c110a7aa1b36676f6a08f8ae337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40845e694ed9e3458871661cb06c7509222d58a1dd6c985f701ffb2bd81a526`

```dockerfile
```

-	Layers:
	-	`sha256:9cd7f5123d62b330090f53d7c7e2b47790328c52a2adf3f1d4eb1ad5b8de3821`  
		Last Modified: Tue, 17 Mar 2026 02:26:32 GMT  
		Size: 2.5 MB (2549910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e72512120a6da3b2c3947c86ab3033ebfe32dc355acf50ff33c08d81207aeb`  
		Last Modified: Tue, 17 Mar 2026 02:26:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json
