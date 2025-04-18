PORTNAME=	solana
DISTVERSIONPREFIX=	v
DISTVERSION=	1.17.9
PORTREVISION=	12
CATEGORIES=	security

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Web-scale blockchain for decentralized apps and marketplaces
WWW=		https://solana.com/ \
		https://github.com/solana-labs/solana

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

BROKEN_armv7=		compilation failure: error[E0512]: cannot transmute between types of different sizes, or dependently-sized types --> programs/bpf_loader/src/syscalls/mod.rs:489:21
BROKEN_i386=		fails on 32-bit systems: https://github.com/solana-labs/solana/issues/16811
BROKEN_powerpc64le=	compilation failure: called `Option::unwrap()` on a `None` value in ring-0.16.20/build.rs:358:10 # see https://github.com/rust-lang/rust/issues/119901

BUILD_DEPENDS=	protoc:devel/protobuf \
		gmake:devel/gmake
LIB_DEPENDS=	libhidapi.so:comms/hidapi

USES=		cargo llvm:lib pkgconfig ssl

USE_GITHUB=	yes
GH_ACCOUNT=	solana-labs

CARGO_CRATES=	Inflector-0.11.4 \
		addr2line-0.20.0 \
		adler-1.0.2 \
		aead-0.4.3 \
		aes-0.7.5 \
		aes-gcm-siv-0.10.3 \
		ahash-0.7.6 \
		ahash-0.8.4 \
		aho-corasick-0.7.18 \
		aho-corasick-1.0.1 \
		aliasable-0.1.3 \
		alloc-no-stdlib-2.0.3 \
		alloc-stdlib-0.2.1 \
		android-tzdata-0.1.1 \
		android_system_properties-0.1.4 \
		anes-0.1.6 \
		ansi_term-0.11.0 \
		anstyle-1.0.1 \
		anyhow-1.0.75 \
		arc-swap-1.5.0 \
		ark-bn254-0.4.0 \
		ark-ec-0.4.2 \
		ark-ff-0.4.2 \
		ark-ff-asm-0.4.2 \
		ark-ff-macros-0.4.2 \
		ark-poly-0.4.2 \
		ark-serialize-0.4.2 \
		ark-serialize-derive-0.4.2 \
		ark-std-0.4.0 \
		array-bytes-1.4.1 \
		arrayref-0.3.7 \
		arrayvec-0.7.4 \
		ascii-0.9.3 \
		asn1-rs-0.5.1 \
		asn1-rs-derive-0.4.0 \
		asn1-rs-impl-0.1.0 \
		assert_cmd-2.0.8 \
		assert_matches-1.5.0 \
		async-channel-1.9.0 \
		async-compression-0.4.1 \
		async-mutex-1.4.0 \
		async-stream-0.3.2 \
		async-stream-impl-0.3.2 \
		async-trait-0.1.74 \
		atty-0.2.14 \
		autocfg-1.1.0 \
		autotools-0.2.5 \
		axum-0.6.20 \
		axum-core-0.3.4 \
		backoff-0.4.0 \
		backtrace-0.3.68 \
		base64-0.12.3 \
		base64-0.13.1 \
		base64-0.21.4 \
		base64ct-1.3.3 \
		bincode-1.3.3 \
		bindgen-0.65.1 \
		bit-set-0.5.2 \
		bit-vec-0.6.3 \
		bitflags-1.3.2 \
		bitflags-2.3.3 \
		bitmaps-2.1.0 \
		blake3-1.5.0 \
		block-buffer-0.7.3 \
		block-buffer-0.9.0 \
		block-buffer-0.10.4 \
		block-padding-0.1.5 \
		block-padding-0.2.1 \
		borsh-0.9.3 \
		borsh-0.10.3 \
		borsh-derive-0.9.3 \
		borsh-derive-0.10.3 \
		borsh-derive-internal-0.9.3 \
		borsh-derive-internal-0.10.3 \
		borsh-schema-derive-internal-0.9.3 \
		borsh-schema-derive-internal-0.10.3 \
		brotli-3.3.4 \
		brotli-decompressor-2.3.2 \
		bs58-0.4.0 \
		bstr-0.2.17 \
		bstr-1.4.0 \
		bumpalo-3.12.0 \
		bv-0.11.1 \
		byte-tools-0.3.1 \
		byte-unit-4.0.19 \
		bytecount-0.6.4 \
		bytemuck-1.14.0 \
		bytemuck_derive-1.4.0 \
		byteorder-1.5.0 \
		bytes-1.5.0 \
		bytesize-1.1.0 \
		bzip2-0.4.4 \
		bzip2-sys-0.1.11+1.0.8 \
		camino-1.0.9 \
		caps-0.5.5 \
		cargo-platform-0.1.2 \
		cargo_metadata-0.15.4 \
		cast-0.2.7 \
		cast-0.3.0 \
		cc-1.0.83 \
		cexpr-0.6.0 \
		cfg-if-0.1.10 \
		cfg-if-1.0.0 \
		chrono-0.4.31 \
		chrono-humanize-0.2.3 \
		ciborium-0.2.1 \
		ciborium-io-0.2.1 \
		ciborium-ll-0.2.1 \
		cipher-0.3.0 \
		clang-sys-1.2.2 \
		clap-2.33.3 \
		clap-3.2.23 \
		clap-4.3.21 \
		clap_builder-4.3.21 \
		clap_derive-3.2.18 \
		clap_lex-0.2.4 \
		clap_lex-0.5.0 \
		combine-3.8.1 \
		concurrent-queue-2.1.0 \
		console-0.15.7 \
		console_error_panic_hook-0.1.7 \
		console_log-0.2.2 \
		const-oid-0.7.1 \
		const_format-0.2.32 \
		const_format_proc_macros-0.2.32 \
		constant_time_eq-0.3.0 \
		convert_case-0.4.0 \
		core-foundation-0.9.2 \
		core-foundation-sys-0.8.3 \
		core_affinity-0.5.10 \
		cpufeatures-0.2.7 \
		crc32fast-1.2.1 \
		criterion-0.5.1 \
		criterion-plot-0.5.0 \
		criterion-stats-0.3.0 \
		crossbeam-channel-0.5.8 \
		crossbeam-deque-0.8.1 \
		crossbeam-utils-0.8.14 \
		crunchy-0.2.2 \
		crypto-common-0.1.3 \
		crypto-mac-0.8.0 \
		csv-1.3.0 \
		csv-core-0.1.11 \
		ctr-0.8.0 \
		ctrlc-3.4.1 \
		curve25519-dalek-3.2.1 \
		darling-0.20.1 \
		darling_core-0.20.1 \
		darling_macro-0.20.1 \
		dashmap-4.0.2 \
		dashmap-5.5.3 \
		data-encoding-2.3.2 \
		der-0.5.1 \
		der-parser-8.1.0 \
		derivation-path-0.2.0 \
		derivative-2.2.0 \
		derive_more-0.99.16 \
		dialoguer-0.10.4 \
		difflib-0.4.0 \
		digest-0.8.1 \
		digest-0.9.0 \
		digest-0.10.7 \
		dir-diff-0.3.2 \
		dirs-next-2.0.0 \
		dirs-sys-next-0.1.2 \
		displaydoc-0.2.3 \
		dlopen2-0.5.0 \
		dlopen2_derive-0.3.0 \
		doc-comment-0.3.3 \
		eager-0.1.0 \
		ed25519-1.2.0 \
		ed25519-dalek-1.0.1 \
		ed25519-dalek-bip32-0.2.0 \
		educe-0.4.18 \
		either-1.9.0 \
		encode_unicode-0.3.6 \
		encoding_rs-0.8.29 \
		enum-iterator-1.4.1 \
		enum-iterator-derive-1.2.1 \
		enum-ordinalize-3.1.10 \
		env_logger-0.9.3 \
		equivalent-1.0.0 \
		errno-0.3.1 \
		errno-dragonfly-0.1.2 \
		etcd-client-0.11.1 \
		event-listener-2.5.2 \
		fake-simd-0.1.2 \
		fast-math-0.1.1 \
		fastrand-2.0.0 \
		fd-lock-3.0.13 \
		feature-probe-0.1.1 \
		filedescriptor-0.8.1 \
		filetime-0.2.15 \
		fixedbitset-0.4.0 \
		flate2-1.0.28 \
		float-cmp-0.9.0 \
		fnv-1.0.7 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		form_urlencoded-1.2.0 \
		fs-err-2.9.0 \
		fs_extra-1.3.0 \
		fuchsia-cprng-0.1.1 \
		futures-0.1.31 \
		futures-0.3.28 \
		futures-channel-0.3.28 \
		futures-core-0.3.28 \
		futures-executor-0.3.28 \
		futures-io-0.3.28 \
		futures-macro-0.3.28 \
		futures-sink-0.3.28 \
		futures-task-0.3.28 \
		futures-util-0.3.28 \
		gag-1.0.0 \
		gdbstub-0.6.3 \
		generic-array-0.12.4 \
		generic-array-0.14.7 \
		gethostname-0.2.3 \
		getrandom-0.1.16 \
		getrandom-0.2.10 \
		gimli-0.27.3 \
		glob-0.3.0 \
		globset-0.4.8 \
		goauth-0.13.1 \
		goblin-0.5.1 \
		h2-0.3.18 \
		half-1.8.2 \
		hash32-0.2.1 \
		hashbrown-0.11.2 \
		hashbrown-0.12.3 \
		hashbrown-0.13.2 \
		hashbrown-0.14.1 \
		headers-0.3.7 \
		headers-core-0.2.0 \
		heck-0.4.0 \
		hermit-abi-0.1.19 \
		hermit-abi-0.3.1 \
		hex-0.4.3 \
		hidapi-2.4.1 \
		histogram-0.6.9 \
		hmac-0.8.1 \
		hmac-0.12.1 \
		hmac-drbg-0.3.0 \
		http-0.2.9 \
		http-body-0.4.5 \
		httparse-1.8.0 \
		httpdate-1.0.1 \
		humantime-2.1.0 \
		hyper-0.14.27 \
		hyper-proxy-0.9.1 \
		hyper-rustls-0.24.1 \
		hyper-timeout-0.4.1 \
		hyper-tls-0.5.0 \
		iana-time-zone-0.1.46 \
		ident_case-1.0.1 \
		idna-0.1.5 \
		idna-0.4.0 \
		ieee754-0.2.6 \
		im-15.1.0 \
		index_list-0.2.7 \
		indexmap-1.9.3 \
		indexmap-2.0.2 \
		indicatif-0.17.7 \
		instant-0.1.12 \
		ipnet-2.3.1 \
		is-terminal-0.4.9 \
		itertools-0.10.5 \
		itoa-1.0.9 \
		jobserver-0.1.24 \
		js-sys-0.3.64 \
		json5-0.4.1 \
		jsonrpc-client-transports-18.0.0 \
		jsonrpc-core-18.0.0 \
		jsonrpc-core-client-18.0.0 \
		jsonrpc-derive-18.0.0 \
		jsonrpc-http-server-18.0.0 \
		jsonrpc-ipc-server-18.0.0 \
		jsonrpc-pubsub-18.0.0 \
		jsonrpc-server-utils-18.0.0 \
		keccak-0.1.0 \
		kernel32-sys-0.2.2 \
		lazy_static-1.4.0 \
		lazycell-1.3.0 \
		libc-0.2.149 \
		libloading-0.7.4 \
		libm-0.2.1 \
		librocksdb-sys-0.11.0+8.1.1 \
		libsecp256k1-0.6.0 \
		libsecp256k1-core-0.2.2 \
		libsecp256k1-gen-ecmult-0.2.1 \
		libsecp256k1-gen-genmult-0.2.1 \
		libz-sys-1.1.3 \
		light-poseidon-0.2.0 \
		linked-hash-map-0.5.4 \
		linux-raw-sys-0.4.3 \
		lock_api-0.4.10 \
		log-0.4.20 \
		lru-0.7.8 \
		lz4-1.24.0 \
		lz4-sys-1.9.4 \
		managed-0.8.0 \
		maplit-1.0.2 \
		matches-0.1.10 \
		matchit-0.7.0 \
		memchr-2.6.3 \
		memmap2-0.5.10 \
		memoffset-0.6.4 \
		memoffset-0.7.1 \
		memoffset-0.9.0 \
		merlin-3.0.0 \
		mime-0.3.16 \
		min-max-heap-1.3.0 \
		minimal-lexical-0.1.4 \
		miniz_oxide-0.7.1 \
		mio-0.8.8 \
		modular-bitfield-0.11.2 \
		modular-bitfield-impl-0.11.2 \
		multimap-0.8.3 \
		native-tls-0.2.11 \
		net2-0.2.37 \
		nix-0.26.4 \
		nix-0.27.1 \
		nom-7.0.0 \
		normalize-line-endings-0.3.0 \
		num-0.2.1 \
		num-bigint-0.2.6 \
		num-bigint-0.4.4 \
		num-complex-0.2.4 \
		num-derive-0.3.3 \
		num-derive-0.4.1 \
		num-integer-0.1.44 \
		num-iter-0.1.43 \
		num-rational-0.2.4 \
		num-traits-0.2.17 \
		num_cpus-1.16.0 \
		num_enum-0.5.11 \
		num_enum-0.6.1 \
		num_enum-0.7.0 \
		num_enum_derive-0.5.11 \
		num_enum_derive-0.6.1 \
		num_enum_derive-0.7.0 \
		num_threads-0.1.3 \
		number_prefix-0.4.0 \
		object-0.31.1 \
		oid-registry-0.6.0 \
		once_cell-1.18.0 \
		oorandom-11.1.3 \
		opaque-debug-0.2.3 \
		opaque-debug-0.3.0 \
		openssl-0.10.57 \
		openssl-macros-0.1.0 \
		openssl-probe-0.1.4 \
		openssl-src-111.25.0+1.1.1t \
		openssl-sys-0.9.92 \
		opentelemetry-0.17.0 \
		os_str_bytes-6.0.0 \
		ouroboros-0.15.6 \
		ouroboros_macro-0.15.6 \
		parity-tokio-ipc-0.9.0 \
		parking_lot-0.11.2 \
		parking_lot-0.12.1 \
		parking_lot_core-0.8.5 \
		parking_lot_core-0.9.8 \
		paste-1.0.9 \
		pbkdf2-0.4.0 \
		pbkdf2-0.11.0 \
		peeking_take_while-0.1.2 \
		pem-1.1.1 \
		percent-encoding-1.0.1 \
		percent-encoding-2.3.0 \
		percentage-0.1.0 \
		pest-2.1.3 \
		pest_derive-2.1.0 \
		pest_generator-2.1.3 \
		pest_meta-2.1.3 \
		petgraph-0.6.0 \
		pickledb-0.5.1 \
		pin-project-1.0.12 \
		pin-project-internal-1.0.12 \
		pin-project-lite-0.2.7 \
		pin-utils-0.1.0 \
		pkcs8-0.8.0 \
		pkg-config-0.3.22 \
		plain-0.2.3 \
		plotters-0.3.4 \
		plotters-backend-0.3.4 \
		plotters-svg-0.3.3 \
		polyval-0.5.3 \
		portable-atomic-1.3.2 \
		ppv-lite86-0.2.15 \
		predicates-2.1.5 \
		predicates-core-1.0.2 \
		predicates-tree-1.0.4 \
		pretty-hex-0.3.0 \
		prettyplease-0.1.9 \
		prettyplease-0.2.4 \
		proc-macro-crate-0.1.5 \
		proc-macro-crate-1.1.0 \
		proc-macro-error-1.0.4 \
		proc-macro-error-attr-1.0.4 \
		proc-macro2-1.0.69 \
		proptest-1.3.1 \
		prost-0.11.9 \
		prost-build-0.11.9 \
		prost-derive-0.11.9 \
		prost-types-0.11.9 \
		protobuf-src-1.1.0+21.5 \
		qstring-0.7.2 \
		qualifier_attr-0.2.2 \
		quick-error-1.2.3 \
		quinn-0.10.2 \
		quinn-proto-0.10.5 \
		quinn-udp-0.4.0 \
		quote-1.0.33 \
		rand-0.4.6 \
		rand-0.7.3 \
		rand-0.8.5 \
		rand_chacha-0.2.2 \
		rand_chacha-0.3.1 \
		rand_core-0.3.1 \
		rand_core-0.4.2 \
		rand_core-0.5.1 \
		rand_core-0.6.4 \
		rand_hc-0.2.0 \
		rand_xorshift-0.3.0 \
		rand_xoshiro-0.6.0 \
		raptorq-1.7.0 \
		rayon-1.8.0 \
		rayon-core-1.12.0 \
		rcgen-0.10.0 \
		rdrand-0.4.0 \
		redox_syscall-0.2.10 \
		redox_syscall-0.3.5 \
		redox_users-0.4.0 \
		reed-solomon-erasure-6.0.0 \
		regex-1.10.2 \
		regex-automata-0.1.10 \
		regex-automata-0.4.3 \
		regex-syntax-0.7.5 \
		regex-syntax-0.8.2 \
		reqwest-0.11.22 \
		ring-0.16.20 \
		rocksdb-0.21.0 \
		rolling-file-0.2.0 \
		rpassword-7.2.0 \
		rtoolbox-0.0.1 \
		rustc-demangle-0.1.21 \
		rustc-hash-1.1.0 \
		rustc_version-0.3.3 \
		rustc_version-0.4.0 \
		rusticata-macros-4.1.0 \
		rustix-0.38.3 \
		rustls-0.21.7 \
		rustls-native-certs-0.6.1 \
		rustls-pemfile-0.2.1 \
		rustls-pemfile-1.0.0 \
		rustls-webpki-0.101.4 \
		rustversion-1.0.14 \
		rusty-fork-0.3.0 \
		ryu-1.0.5 \
		same-file-1.0.6 \
		schannel-0.1.19 \
		scopeguard-1.2.0 \
		scroll-0.11.0 \
		scroll_derive-0.11.0 \
		sct-0.7.0 \
		security-framework-2.4.2 \
		security-framework-sys-2.4.2 \
		semver-0.11.0 \
		semver-1.0.20 \
		semver-parser-0.10.2 \
		serde-1.0.189 \
		serde_bytes-0.11.12 \
		serde_derive-1.0.189 \
		serde_json-1.0.107 \
		serde_urlencoded-0.7.1 \
		serde_with-2.3.3 \
		serde_with_macros-2.3.3 \
		serde_yaml-0.8.26 \
		serde_yaml-0.9.25 \
		serial_test-2.0.0 \
		serial_test_derive-2.0.0 \
		sha-1-0.8.2 \
		sha-1-0.9.8 \
		sha-1-0.10.0 \
		sha1-0.10.5 \
		sha2-0.9.9 \
		sha2-0.10.8 \
		sha3-0.9.1 \
		sha3-0.10.4 \
		sharded-slab-0.1.4 \
		shell-words-1.1.0 \
		shlex-1.1.0 \
		signal-hook-0.3.17 \
		signal-hook-registry-1.4.0 \
		signature-1.4.0 \
		simpl-0.1.0 \
		siphasher-0.3.11 \
		sized-chunks-0.6.5 \
		slab-0.4.5 \
		smallvec-1.11.1 \
		smpl_jwt-0.7.1 \
		socket2-0.4.9 \
		socket2-0.5.5 \
		soketto-0.7.1 \
		solana_rbpf-0.8.0 \
		spin-0.5.2 \
		spin-0.9.2 \
		spki-0.5.4 \
		spl-associated-token-account-2.2.0 \
		spl-discriminator-0.1.0 \
		spl-discriminator-derive-0.1.1 \
		spl-discriminator-syn-0.1.1 \
		spl-instruction-padding-0.1.0 \
		spl-memo-4.0.0 \
		spl-pod-0.1.0 \
		spl-program-error-0.3.0 \
		spl-program-error-derive-0.3.1 \
		spl-tlv-account-resolution-0.4.0 \
		spl-token-4.0.0 \
		spl-token-2022-0.9.0 \
		spl-token-metadata-interface-0.2.0 \
		spl-transfer-hook-interface-0.3.0 \
		spl-type-length-value-0.3.0 \
		static_assertions-1.1.0 \
		stream-cancel-0.8.1 \
		strsim-0.8.0 \
		strsim-0.10.0 \
		strum-0.24.0 \
		strum_macros-0.24.3 \
		subtle-2.4.1 \
		symlink-0.1.0 \
		syn-1.0.109 \
		syn-2.0.38 \
		sync_wrapper-0.1.1 \
		synstructure-0.12.6 \
		sys-info-0.9.1 \
		sysctl-0.4.6 \
		system-configuration-0.5.1 \
		system-configuration-sys-0.5.0 \
		systemstat-0.2.3 \
		tar-0.4.40 \
		tarpc-0.29.0 \
		tarpc-plugins-0.12.0 \
		tempfile-3.8.0 \
		termcolor-1.1.2 \
		termtree-0.2.3 \
		test-case-3.2.1 \
		test-case-core-3.2.1 \
		test-case-macros-3.2.1 \
		textwrap-0.11.0 \
		textwrap-0.16.0 \
		thiserror-1.0.50 \
		thiserror-impl-1.0.50 \
		thread-scoped-1.0.2 \
		thread_local-1.1.4 \
		tikv-jemalloc-sys-0.4.2+5.2.1-patched.2 \
		tikv-jemallocator-0.4.1 \
		time-0.3.9 \
		time-macros-0.2.4 \
		tiny-bip39-0.8.2 \
		tinytemplate-1.2.1 \
		tinyvec-1.5.0 \
		tinyvec_macros-0.1.0 \
		tokio-1.29.1 \
		tokio-io-timeout-1.1.1 \
		tokio-macros-2.1.0 \
		tokio-native-tls-0.3.0 \
		tokio-rustls-0.24.1 \
		tokio-serde-0.8.0 \
		tokio-stream-0.1.14 \
		tokio-tungstenite-0.20.1 \
		tokio-util-0.6.9 \
		tokio-util-0.7.1 \
		toml-0.5.8 \
		tonic-0.9.2 \
		tonic-build-0.9.2 \
		tower-0.4.13 \
		tower-layer-0.3.2 \
		tower-service-0.3.2 \
		tracing-0.1.29 \
		tracing-attributes-0.1.18 \
		tracing-core-0.1.21 \
		tracing-opentelemetry-0.17.2 \
		tracing-subscriber-0.3.7 \
		trees-0.4.2 \
		try-lock-0.2.3 \
		tungstenite-0.20.1 \
		typenum-1.15.0 \
		ucd-trie-0.1.3 \
		unarray-0.1.4 \
		unicase-2.6.0 \
		unicode-bidi-0.3.13 \
		unicode-ident-1.0.2 \
		unicode-normalization-0.1.22 \
		unicode-width-0.1.9 \
		unicode-xid-0.2.2 \
		universal-hash-0.4.1 \
		unreachable-1.0.0 \
		unsafe-libyaml-0.2.8 \
		untrusted-0.7.1 \
		uriparse-0.6.4 \
		url-1.7.2 \
		url-2.4.1 \
		utf-8-0.7.6 \
		utf8-width-0.1.5 \
		vcpkg-0.2.15 \
		vec_map-0.8.2 \
		version_check-0.9.4 \
		void-1.0.2 \
		wait-timeout-0.2.0 \
		walkdir-2.3.2 \
		want-0.3.0 \
		wasi-0.9.0+wasi-snapshot-preview1 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		wasm-bindgen-0.2.87 \
		wasm-bindgen-backend-0.2.87 \
		wasm-bindgen-futures-0.4.28 \
		wasm-bindgen-macro-0.2.87 \
		wasm-bindgen-macro-support-0.2.87 \
		wasm-bindgen-shared-0.2.87 \
		web-sys-0.3.55 \
		webpki-roots-0.24.0 \
		webpki-roots-0.25.2 \
		which-4.2.2 \
		winapi-0.2.8 \
		winapi-0.3.9 \
		winapi-build-0.1.1 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.5 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-sys-0.45.0 \
		windows-sys-0.48.0 \
		windows-targets-0.42.2 \
		windows-targets-0.48.0 \
		windows_aarch64_gnullvm-0.42.2 \
		windows_aarch64_gnullvm-0.48.0 \
		windows_aarch64_msvc-0.42.2 \
		windows_aarch64_msvc-0.48.0 \
		windows_i686_gnu-0.42.2 \
		windows_i686_gnu-0.48.0 \
		windows_i686_msvc-0.42.2 \
		windows_i686_msvc-0.48.0 \
		windows_x86_64_gnu-0.42.2 \
		windows_x86_64_gnu-0.48.0 \
		windows_x86_64_gnullvm-0.42.2 \
		windows_x86_64_gnullvm-0.48.0 \
		windows_x86_64_msvc-0.42.2 \
		windows_x86_64_msvc-0.48.0 \
		winreg-0.50.0 \
		x509-parser-0.14.0 \
		xattr-1.0.1 \
		yaml-rust-0.4.5 \
		yasna-0.5.0 \
		zerocopy-0.7.11 \
		zerocopy-derive-0.7.11 \
		zeroize-1.3.0 \
		zeroize_derive-1.4.2 \
		zstd-0.11.2+zstd.1.5.2 \
		zstd-safe-5.0.1+zstd.1.5.2 \
		zstd-sys-2.0.1+zstd.1.5.2 \
		crossbeam-epoch@git+https://github.com/solana-labs/crossbeam?rev=fd279d707025f0e60951e429bf778b4813d1b6bf\#fd279d707025f0e60951e429bf778b4813d1b6bf

XARCH=		${ARCH:S/amd64/x86_64/:tu}

MAKE_ENV=	${XARCH}_UNKNOWN_FREEBSD_OPENSSL_INCLUDE_DIR=${OPENSSLINC} \
		${XARCH}_UNKNOWN_FREEBSD_OPENSSL_LIB_DIR=${OPENSSLLIB}

BINARY_ALIAS=	llvm-config=${LOCALBASE}/bin/${LLVM_CONFIG}

do-install:
	for f in ${CARGO_TARGET_DIR}/*/${PORTNAME}*; do \
		if [ -f $$f -a -x $$f ]; then \
			${INSTALL_PROGRAM} $$f ${STAGEDIR}${PREFIX}/bin; \
		fi \
	done

do-test:
	@${CARGO_CARGO_RUN} test

.include <bsd.port.mk>
