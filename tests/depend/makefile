include $(d)../../src/prorab.mk

ifneq ($(strip $(call prorab-depend, hello, /world/number_one)),$(abspath $(d)hello): $(prorab_fs_root)world/number_one)
    $(error prorab-depend test 1 failed: $(strip $(call prorab-depend, hello, /world/number_one)))
endif

ifneq ($(strip $(call prorab-depend, hello, /world/number_one /world/number_two)),$(abspath $(d)hello): $(prorab_fs_root)world/number_one $(prorab_fs_root)world/number_two)
    $(error prorab-depend test 2 failed: $(strip $(call prorab-depend, hello, /world/number_one /world/number_two)))
endif

ifneq ($(strip $(call prorab-depend, /hello, world/number_three ../world/number_four)),/hello: $(abspath $(d)world/number_three) $(abspath $(d)../world/number_four))
    $(error prorab-depend test 3 failed)
endif
