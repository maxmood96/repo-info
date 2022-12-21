## `aerospike:ee-6.1.0.3`

```console
$ docker pull aerospike@sha256:36f1423ecb4655ef94fb9a835d53004eb60dd8d97fdfd64abaa2be1b5525cdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:ce5b00c6c02f20a56c6a3050b83e22aff0f562c2498b49ecbbcc43849609b513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68152826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1b895e58d86706e8cc88f208a2743ed312ba32063d28aae972058e9f098426`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:45:26 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Wed, 21 Dec 2022 01:45:26 GMT
ENV AEROSPIKE_SHA256=de62082abe7c5fb040fc5eaaed22274142d96cbcd7dfce7530a52d65bce8b277
# Wed, 21 Dec 2022 01:45:26 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Wed, 21 Dec 2022 01:45:26 GMT
SHELL [/bin/bash -o pipefail -c]
# Wed, 21 Dec 2022 01:45:43 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && apt-get install -y --no-install-recommends     libcurl4     libldap-2.4.2   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Wed, 21 Dec 2022 01:45:44 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Wed, 21 Dec 2022 01:45:44 GMT
COPY file:954d06187376ade36d0a4daf43c9abe4806362f2f33f0bd9dbaef5a67c967bd3 in /entrypoint.sh 
# Wed, 21 Dec 2022 01:45:44 GMT
EXPOSE 3000 3001 3002
# Wed, 21 Dec 2022 01:45:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 21 Dec 2022 01:45:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e1d68d4750747bd8885c971b7516be42c60573aa09d1ae9f04f68303261c5b`  
		Last Modified: Wed, 21 Dec 2022 01:46:21 GMT  
		Size: 36.8 MB (36754018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52428c3e5ff5f33f8fe9a2cff73f144ea07f6c1634c9e58f0bc7d39c48c5e1ef`  
		Last Modified: Wed, 21 Dec 2022 01:46:15 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3dd6e52eeb25336d075fc81af832da788a2b6b3622388f650a7946b9d60f0d`  
		Last Modified: Wed, 21 Dec 2022 01:46:15 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
