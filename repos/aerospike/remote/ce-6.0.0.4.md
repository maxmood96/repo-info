## `aerospike:ce-6.0.0.4`

```console
$ docker pull aerospike@sha256:f6b0219cd13dab0ed2cb95fb183f737a116f1303ed1c99a5a04650b06c0aa45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:f37160640406c505a30ddf708bb2f0cfc1c9b11b8d784b0c2363fff9ebcfa24f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101870742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8dc8ea9bac2a3042d948fe88ee247ede58db7ad4f03e332badadcdf5a393c`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:44:08 GMT
ENV AEROSPIKE_VERSION=6.0.0.4
# Tue, 23 Aug 2022 00:44:36 GMT
ENV AEROSPIKE_SHA256=df05478abc56add36a14c9fbed315d35a641061295493d26cc98a5637ba23d4b
# Tue, 23 Aug 2022 00:44:57 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 23 Aug 2022 00:44:58 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 23 Aug 2022 00:44:58 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Tue, 23 Aug 2022 00:44:58 GMT
EXPOSE 3000 3001 3002
# Tue, 23 Aug 2022 00:44:58 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 23 Aug 2022 00:44:58 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff337ca20891f56235ffcb66cedc0a60e4345ca6ad0eec0cd525163a342e5f`  
		Last Modified: Tue, 23 Aug 2022 00:45:41 GMT  
		Size: 74.7 MB (74730584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f75c341ea4692d3260702e8f0a14be5ccff6999d9fccd37781ab580a0d6b62`  
		Last Modified: Tue, 23 Aug 2022 00:45:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ed9d065c33bd12e58567bf5fdb65ff24fcc0db3e7d7629526523de297e01e9`  
		Last Modified: Tue, 23 Aug 2022 00:45:30 GMT  
		Size: 810.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
