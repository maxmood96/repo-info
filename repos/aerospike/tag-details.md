<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.0.0.5`](#aerospikece-6005)
-	[`aerospike:ee-6.0.0.5`](#aerospikeee-6005)

## `aerospike:ce-6.0.0.5`

```console
$ docker pull aerospike@sha256:de3e7000f002dabba40c9e4483fb27b577f2fba5fcf89b525eaf0b03a14e4292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:dfb3e79d1ffcf2cf4f09bccce2ece7e4921d6c3ca6b93a099d77690ba4acf909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120640645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6316ec53c9be62d30e155d6887b29561ede28b8edba38520d93f0ba077f62`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_VERSION=6.0.0.5
# Wed, 24 Aug 2022 23:07:30 GMT
ENV AEROSPIKE_SHA256=2eb30e08fd5fa5055e328ee5e652f59efd99af66f2b9e8eede5ffb532b7bd99a
# Wed, 24 Aug 2022 23:07:52 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 24 Aug 2022 23:07:53 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Wed, 24 Aug 2022 23:07:53 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Wed, 24 Aug 2022 23:07:53 GMT
EXPOSE 3000 3001 3002
# Wed, 24 Aug 2022 23:07:53 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 24 Aug 2022 23:07:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881157797cddbdeff8b21fb4836cb9edf326fc5b4f78000ddfbb71141b7633a7`  
		Last Modified: Wed, 24 Aug 2022 23:08:38 GMT  
		Size: 93.5 MB (93500485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e5498ad9c5c229735d5961958b4fc55ec046b9121b203dd4429c9f5a42e6e8`  
		Last Modified: Wed, 24 Aug 2022 23:08:25 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d5a9b1714a60625c3ef8d697cc1ddd4698f250998c51d94948da3cc3f7894b`  
		Last Modified: Wed, 24 Aug 2022 23:08:25 GMT  
		Size: 810.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.0.0.5`

```console
$ docker pull aerospike@sha256:e6b0ec10e3dcd4ffae4ac93f13a48e87a126b418a7f3d45e800d1afabb9c712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:4dc5367eb041cc1e7367a3eb1a437c2b4fa0d3c333d629030d516f5c3b9741c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123034000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a82fe84536d4e93f326013a03bfff5125786b2c71481d0e77bf38f122e1ab`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_VERSION=6.0.0.5
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_SHA256=3b40c4aec82a93e1b2d04db47efce7d7a5f7ad29c82f66cf1d0c83775f5f4f9c
# Wed, 24 Aug 2022 23:07:03 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Wed, 24 Aug 2022 23:07:27 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 24 Aug 2022 23:07:28 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Wed, 24 Aug 2022 23:07:28 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Wed, 24 Aug 2022 23:07:28 GMT
EXPOSE 3000 3001 3002
# Wed, 24 Aug 2022 23:07:28 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 24 Aug 2022 23:07:28 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e391a17b4eb19736dae7a745a99c2331ce4435b148983d18783ffff186ba39c`  
		Last Modified: Wed, 24 Aug 2022 23:08:18 GMT  
		Size: 95.9 MB (95893789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a0153a329f3e7ec67d1227c7389d7004e088048cc369146b791ac4666fa261`  
		Last Modified: Wed, 24 Aug 2022 23:08:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8e5cd9ecf15abd5b47c0fcfa8f0ade09c344c7012ed068b225f32f85283eee`  
		Last Modified: Wed, 24 Aug 2022 23:08:04 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
