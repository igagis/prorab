include $(d)../../../src/prorab.mk

$(eval $(call prorab-config,../config))

define this_rules
    all: gen_out

    .PHONY:
    gen_out:
$(.RECIPEPREFIX)$(a)mkdir -p $(d)$(this_out_dir)
$(.RECIPEPREFIX)$(a)echo "hello prorab" > $(d)$(this_out_dir)out.txt
    clean::
$(.RECIPEPREFIX)$(a)rm -f $(d)$(this_out_dir)out.txt
endef
$(eval $(this_rules))

# test including makefile with different config
$(eval $(call prorab-include, makefile2, dbg))
